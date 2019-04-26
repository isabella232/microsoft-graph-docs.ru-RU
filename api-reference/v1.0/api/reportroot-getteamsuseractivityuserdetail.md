---
title: 'reportRoot: getTeamsUserActivityUserDetail'
description: Получение сведений о действиях отдельных пользователей Microsoft Teams.
localization_priority: Priority
ms.prod: reports
author: pranoychaudhuri
ms.openlocfilehash: fdc9976847085eeea99ff504862a97450aea9a1b
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32572789"
---
# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="41ece-103">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="41ece-103">reportRoot: getTeamsUserActivityUserDetail</span></span>

<span data-ttu-id="41ece-104">Получение сведений о действиях отдельных пользователей Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="41ece-104">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="41ece-105">Разрешения</span><span class="sxs-lookup"><span data-stu-id="41ece-105">Permissions</span></span>

<span data-ttu-id="41ece-p101">Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41ece-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="41ece-108">Тип разрешения</span><span class="sxs-lookup"><span data-stu-id="41ece-108">Permission type</span></span>                        | <span data-ttu-id="41ece-109">Разрешения (в порядке повышения привилегий)</span><span class="sxs-lookup"><span data-stu-id="41ece-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="41ece-110">Делегированные (рабочая или учебная учетная запись)</span><span class="sxs-lookup"><span data-stu-id="41ece-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="41ece-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="41ece-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="41ece-112">Делегированные (личная учетная запись Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="41ece-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41ece-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41ece-113">Not supported.</span></span>                           |
| <span data-ttu-id="41ece-114">Для приложений</span><span class="sxs-lookup"><span data-stu-id="41ece-114">Application</span></span>                            | <span data-ttu-id="41ece-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="41ece-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="41ece-116">HTTP-запрос</span><span class="sxs-lookup"><span data-stu-id="41ece-116">HTTP request</span></span>

<!-- { "blockType": "samples" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='{period_value}')
GET /reports/getTeamsUserActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="41ece-117">Параметры функции</span><span class="sxs-lookup"><span data-stu-id="41ece-117">Function parameters</span></span>

<span data-ttu-id="41ece-118">В URL-адресе запроса укажите один из приведенных ниже параметров и действительное значение.</span><span class="sxs-lookup"><span data-stu-id="41ece-118">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="41ece-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="41ece-119">Parameter</span></span> | <span data-ttu-id="41ece-120">Тип</span><span class="sxs-lookup"><span data-stu-id="41ece-120">Type</span></span>   | <span data-ttu-id="41ece-121">Описание</span><span class="sxs-lookup"><span data-stu-id="41ece-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="41ece-122">period</span><span class="sxs-lookup"><span data-stu-id="41ece-122">period</span></span>    | <span data-ttu-id="41ece-123">string</span><span class="sxs-lookup"><span data-stu-id="41ece-123">string</span></span> | <span data-ttu-id="41ece-124">Указывает отчетный период.</span><span class="sxs-lookup"><span data-stu-id="41ece-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="41ece-125">Поддерживаемые значения {period_value}: D7, D30, D90 и D180.</span><span class="sxs-lookup"><span data-stu-id="41ece-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="41ece-126">Эти значения указываются в формате D*n*, где *n* — количество дней в отчетном периоде.</span><span class="sxs-lookup"><span data-stu-id="41ece-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="41ece-127">date</span><span class="sxs-lookup"><span data-stu-id="41ece-127">date</span></span>      | <span data-ttu-id="41ece-128">Date</span><span class="sxs-lookup"><span data-stu-id="41ece-128">Date</span></span>   | <span data-ttu-id="41ece-129">Указывает дату, за которую вы хотите просмотреть пользователей, выполнивших какое-либо действие.</span><span class="sxs-lookup"><span data-stu-id="41ece-129">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="41ece-130">Значение {date_value} указывается в формате ГГГГ-ММ-ДД.</span><span class="sxs-lookup"><span data-stu-id="41ece-130">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="41ece-131">Так как этот отчет доступен только за последние 30 дней, значение {date_value} должно быть датой из этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="41ece-131">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="41ece-132">**Примечание.** В URL-адресе необходимо указать либо период, либо дату.</span><span class="sxs-lookup"><span data-stu-id="41ece-132">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="41ece-133">Заголовки запросов</span><span class="sxs-lookup"><span data-stu-id="41ece-133">Request headers</span></span>

| <span data-ttu-id="41ece-134">Имя</span><span class="sxs-lookup"><span data-stu-id="41ece-134">Name</span></span>          | <span data-ttu-id="41ece-135">Описание</span><span class="sxs-lookup"><span data-stu-id="41ece-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="41ece-136">Авторизация</span><span class="sxs-lookup"><span data-stu-id="41ece-136">Authorization</span></span> | <span data-ttu-id="41ece-p104">Bearer {токен}. Обязательный.</span><span class="sxs-lookup"><span data-stu-id="41ece-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="41ece-139">Отклик</span><span class="sxs-lookup"><span data-stu-id="41ece-139">Response</span></span>

<span data-ttu-id="41ece-140">В случае успешного выполнения этот метод возвращает отклик `302 Found`, который перенаправляет на URL-адрес, для которого выполнена предварительная аутентификация, для скачивания отчета.</span><span class="sxs-lookup"><span data-stu-id="41ece-140">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="41ece-141">Этот URL-адрес можно найти в заголовке `Location` отклика.</span><span class="sxs-lookup"><span data-stu-id="41ece-141">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="41ece-142">URL-адреса для скачивания, для которых выполнена предварительная аутентификация, действительны в течение нескольких минут и не требуют заголовка `Authorization`.</span><span class="sxs-lookup"><span data-stu-id="41ece-142">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="41ece-143">CSV-файл содержит столбцы со следующими заголовками:</span><span class="sxs-lookup"><span data-stu-id="41ece-143">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="41ece-144">Report Refresh Date (Дата обновления отчета);</span><span class="sxs-lookup"><span data-stu-id="41ece-144">Report Refresh Date</span></span>
- <span data-ttu-id="41ece-145">"User Principal Name" (Имя участника-пользователя);</span><span class="sxs-lookup"><span data-stu-id="41ece-145">User Principal Name</span></span>
- <span data-ttu-id="41ece-146">Last Activity Date (Дата последнего действия);</span><span class="sxs-lookup"><span data-stu-id="41ece-146">Last Activity Date</span></span>
- <span data-ttu-id="41ece-147">Is Deleted (Удален);</span><span class="sxs-lookup"><span data-stu-id="41ece-147">Is Deleted</span></span>
- <span data-ttu-id="41ece-148">Deleted Date (Дата удаления);</span><span class="sxs-lookup"><span data-stu-id="41ece-148">Deleted Date</span></span>
- <span data-ttu-id="41ece-149">Assigned Products (Назначенные продукты);</span><span class="sxs-lookup"><span data-stu-id="41ece-149">Assigned Products</span></span>
- <span data-ttu-id="41ece-150">Team Chat Messages Count (Количество сообщений в чатах групп);</span><span class="sxs-lookup"><span data-stu-id="41ece-150">Team Chat Message Count</span></span>
- <span data-ttu-id="41ece-151">Private Chat Message Count (Количество сообщений в приватных чатах);</span><span class="sxs-lookup"><span data-stu-id="41ece-151">Private Chat Message Count</span></span>
- <span data-ttu-id="41ece-152">Call Count (Количество звонков);</span><span class="sxs-lookup"><span data-stu-id="41ece-152">Call Count</span></span>
- <span data-ttu-id="41ece-153">Meeting Count (Количество собраний);</span><span class="sxs-lookup"><span data-stu-id="41ece-153">Meeting Count</span></span>
- <span data-ttu-id="41ece-154">Has Other Action (Есть другое действие);</span><span class="sxs-lookup"><span data-stu-id="41ece-154">Has Other Action</span></span>
- <span data-ttu-id="41ece-155">Report Period (Отчетный период).</span><span class="sxs-lookup"><span data-stu-id="41ece-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="41ece-156">Пример</span><span class="sxs-lookup"><span data-stu-id="41ece-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="41ece-157">Запрос</span><span class="sxs-lookup"><span data-stu-id="41ece-157">Request</span></span>

<span data-ttu-id="41ece-158">Ниже приведен пример запроса.</span><span class="sxs-lookup"><span data-stu-id="41ece-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="41ece-159">Отклик</span><span class="sxs-lookup"><span data-stu-id="41ece-159">Response</span></span>

<span data-ttu-id="41ece-160">Ниже приведен пример отклика.</span><span class="sxs-lookup"><span data-stu-id="41ece-160">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="41ece-161">У скачанного после перенаправления 302 CSV-файла будет приведенная ниже схема.</span><span class="sxs-lookup"><span data-stu-id="41ece-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```
