---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112036"
---
# <span data-ttu-id="49813-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="49813-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="49813-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49813-102">SYNOPSIS</span></span>
<span data-ttu-id="49813-103">Cria um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-103">Creates a support ticket.</span></span>

## <span data-ttu-id="49813-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49813-104">SYNTAX</span></span>

### <span data-ttu-id="49813-105">CreateSupportTicketWithContactDetailParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="49813-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49813-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49813-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49813-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49813-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49813-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49813-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49813-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="49813-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49813-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="49813-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49813-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49813-111">DESCRIPTION</span></span>
<span data-ttu-id="49813-112">Este cmdlet pode ser usado para criar um tíquete de suporte para cobrança, gerenciamento de assinaturas, cotas ou problemas técnicos.</span><span class="sxs-lookup"><span data-stu-id="49813-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="49813-113">Use cmdlets Get-AzSupportService e Get-AzSupportProblemClassification para identificar o serviço do Azure e ele tem classificações de problemas correspondentes, respectivamente para as quais você deseja solicitar suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="49813-114">Você deve especificar os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="49813-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="49813-115">Você pode usar o cmdlet do auxiliar New-AzSupportContactProfileObject para criar o objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="49813-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="49813-116">Os provedores de soluções na nuvem podem criar um tíquete de suporte para as assinaturas do cliente conectando ao locatário do cliente e especificando sua ID de locatário inicial usando o parâmetro *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="49813-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="49813-117">__Para tíquetes técnicos:__</span><span class="sxs-lookup"><span data-stu-id="49813-117">__For technical tickets:__</span></span>

<span data-ttu-id="49813-118">Para especificar o nome do recurso, especifique a ID do recurso ARM do recurso usando o parâmetro *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="49813-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="49813-119">Veja um exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="49813-119">See an example below.</span></span> 

<span data-ttu-id="49813-120">__Para tíquetes de cota:__</span><span class="sxs-lookup"><span data-stu-id="49813-120">__For quota tickets:__</span></span>

<span data-ttu-id="49813-121">Para solicitar aumento de cota para **núcleos de VM de computação** , **lote** , banco de dados **SQL** e **SQL data warehouse** , forneça detalhes adicionais em objeto *QuotaTicketDetail* .</span><span class="sxs-lookup"><span data-stu-id="49813-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="49813-122">O objeto QuotaTicketDetail consiste em 3 propriedades conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="49813-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="49813-123">Para obter documentação detalhada, [clique aqui.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="49813-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="49813-124">Para obter documentação detalhada sobre como construir carga para vários tipos de cotas, [clique aqui](https://aka.ms/supportrpquotarequestpayload) .</span><span class="sxs-lookup"><span data-stu-id="49813-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="49813-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49813-125">EXAMPLES</span></span>

### <span data-ttu-id="49813-126">Exemplo 1: criar um tíquete de suporte para gerenciamento de faturamento ou assinatura.</span><span class="sxs-lookup"><span data-stu-id="49813-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="49813-127">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas de gerenciamento de assinaturas ou cobrança para a qual você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="49813-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-128">Exemplo 2: criar um tíquete de suporte técnico para o recurso da máquina virtual para Windows.</span><span class="sxs-lookup"><span data-stu-id="49813-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="49813-129">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas para a máquina virtual para Windows para as quais você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="49813-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-130">Exemplo 3: criar um tíquete de suporte de cotas para aumentar a cota de núcleos de máquina virtual para uma família específica de VM.</span><span class="sxs-lookup"><span data-stu-id="49813-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="49813-131">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas de núcleos de VM de computação de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-132">Exemplo 4: criar um tíquete de suporte de cotas para aumentar a cota de núcleos de baixa prioridade para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="49813-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="49813-133">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para classificação de problemas em lotes de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-134">Exemplo 5: criar um tíquete de suporte de cotas para aumentar a cota de núcleos de VM para uma família específica de VMs para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="49813-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="49813-135">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para classificação de problemas em lotes de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-136">Exemplo 6: criar um tíquete de suporte de cotas para aumentar a cota de grupos para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="49813-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="49813-137">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para classificação de problemas em lotes de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-138">Exemplo 7: criar um tíquete de suporte de cotas para aumentar trabalhos ativos e cota de cronogramas de trabalho para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="49813-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="49813-139">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para classificação de problemas em lotes de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-140">Exemplo 8: criar um tíquete de suporte de cotas para aumentar o número de contas em lotes para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="49813-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="49813-141">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para classificação de problemas em lotes de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-142">Exemplo 9: criar um tíquete de suporte de cotas para aumentar a cota de DTUs para o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="49813-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="49813-143">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas do banco de dados SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-144">Exemplo 10: criar um tíquete de suporte de cotas para aumentar a cota de servidores para o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="49813-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="49813-145">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas do banco de dados SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-146">Exemplo 11: criar um tíquete de suporte de cotas para aumentar a cota de DTUs para SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="49813-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="49813-147">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas de depósito de data SQL da cota.</span><span class="sxs-lookup"><span data-stu-id="49813-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-148">Exemplo 12: criar um tíquete de suporte de cotas para aumentar a cota de servidores para SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="49813-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="49813-149">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas de data warehouse do SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-150">Exemplo 13: criar um tíquete de suporte de cotas para aumentar a cota de núcleos de baixa prioridade para o serviço de aprendizagem de máquina.</span><span class="sxs-lookup"><span data-stu-id="49813-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="49813-151">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação do problema do serviço de aprendizagem da máquina de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-152">Exemplo 14: criar um tíquete de suporte de cotas para aumentar a cota de núcleos de VM para uma família específica de VMs para serviço de aprendizagem de computador.</span><span class="sxs-lookup"><span data-stu-id="49813-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="49813-153">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação do problema do serviço de aprendizagem da máquina de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-154">Exemplo 15: criar um tíquete de suporte de cotas para aumentar a cota de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="49813-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="49813-155">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos da classificação de problemas do serviço de instância gerenciada SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="49813-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-156">Exemplo 16: criar um tíquete de suporte especificando parâmetros de contato do cliente individuais em vez do objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="49813-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-157">Exemplo 17: criar um tíquete de suporte com solicitação de resposta 24 x 7 do Azure.</span><span class="sxs-lookup"><span data-stu-id="49813-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="49813-158">Exemplo 18: criar um tíquete de suporte em nome de seu cliente se você for um provedor de soluções de nuvem (CSP).</span><span class="sxs-lookup"><span data-stu-id="49813-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="49813-159">O CSP deve primeiro fazer login no locatário dele e, em seguida, fazer logon no locatário do cliente, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="49813-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="49813-160">Eles devem usar o parâmetro-CSPHomeTenantId para especificar sua ID de locatário inicial no momento da criação de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="49813-161">OS</span><span class="sxs-lookup"><span data-stu-id="49813-161">PARAMETERS</span></span>

### <span data-ttu-id="49813-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="49813-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="49813-163">Endereços de email adicionais.</span><span class="sxs-lookup"><span data-stu-id="49813-163">Additional email addresses.</span></span>
<span data-ttu-id="49813-164">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49813-165">-AsJob</span></span>
<span data-ttu-id="49813-166">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="49813-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="49813-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="49813-168">Esta é a ID do locatário inicial do usuário do provedor de soluções na nuvem que está tentando criar um tíquete de suporte para o cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="49813-169">-CustomerContactDetail</span></span>
<span data-ttu-id="49813-170">Detalhes de contato do cliente associados ao recurso SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="49813-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="49813-171">-CustomerCountry</span></span>
<span data-ttu-id="49813-172">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-172">Customer country.</span></span>
<span data-ttu-id="49813-173">Deve ser um código de país Alfa-3 ISO válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="49813-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="49813-174">-CustomerFirstName</span></span>
<span data-ttu-id="49813-175">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="49813-176">-CustomerLastName</span></span>
<span data-ttu-id="49813-177">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="49813-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="49813-179">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-179">Customer phone number.</span></span>
<span data-ttu-id="49813-180">Isso será necessário se o método de contato preferencial for o telefone.</span><span class="sxs-lookup"><span data-stu-id="49813-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="49813-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="49813-182">Idioma Peferred do personalizado.</span><span class="sxs-lookup"><span data-stu-id="49813-182">Peferred language of the custom.</span></span>
<span data-ttu-id="49813-183">Deve ser um código de conta de idioma válido para um dos idiomas com suporte listados aqui https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="49813-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="49813-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="49813-185">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-185">Customer preferred time zone.</span></span>
<span data-ttu-id="49813-186">Deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="49813-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="49813-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="49813-188">Endereço de e-mail principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="49813-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49813-189">-DefaultProfile</span></span>
<span data-ttu-id="49813-190">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49813-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-191">-Descrição</span><span class="sxs-lookup"><span data-stu-id="49813-191">-Description</span></span>
<span data-ttu-id="49813-192">Descrição detalhada da pergunta ou do problema.</span><span class="sxs-lookup"><span data-stu-id="49813-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-193">-Nome</span><span class="sxs-lookup"><span data-stu-id="49813-193">-Name</span></span>
<span data-ttu-id="49813-194">Nome da permissão de suporte que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="49813-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="49813-195">-PreferredContactMethod</span></span>
<span data-ttu-id="49813-196">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="49813-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="49813-197">-ProblemClassificationId</span></span>
<span data-ttu-id="49813-198">Cada serviço do Azure tem seu próprio conjunto de categorias de problemas chamado classificação de problemas que corresponde ao tipo de problema que você está enfrentando.</span><span class="sxs-lookup"><span data-stu-id="49813-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="49813-199">Esse parâmetro é a ID do recurso ARM do recurso ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="49813-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="49813-200">-ProblemStartTime</span></span>
<span data-ttu-id="49813-201">Data e hora em que o problema foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="49813-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="49813-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="49813-203">Detalhes adicionais de um tíquete de suporte à cota.</span><span class="sxs-lookup"><span data-stu-id="49813-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="49813-204">-Require24X7Response</span></span>
<span data-ttu-id="49813-205">Indica se esse tíquete de suporte requer uma resposta 24x7 do Azure.</span><span class="sxs-lookup"><span data-stu-id="49813-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-206">-Severidade</span><span class="sxs-lookup"><span data-stu-id="49813-206">-Severity</span></span>
<span data-ttu-id="49813-207">Gravidade do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-207">Severity of the support ticket.</span></span>
<span data-ttu-id="49813-208">Isso indica a urgência do caso, que, por sua vez, determina o tempo de resposta de acordo com o contrato de nível de serviço do plano de suporte técnico que você tem com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49813-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="49813-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="49813-210">Esta é a ID do recurso do serviço do Azure (por exemplo: um recurso de máquina virtual ou um recurso HDInsight) para o qual o tíquete de suporte é criado.</span><span class="sxs-lookup"><span data-stu-id="49813-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-211">-Título</span><span class="sxs-lookup"><span data-stu-id="49813-211">-Title</span></span>
<span data-ttu-id="49813-212">Título do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="49813-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-213">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49813-213">-Confirm</span></span>
<span data-ttu-id="49813-214">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49813-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49813-215">-WhatIf</span></span>
<span data-ttu-id="49813-216">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49813-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49813-217">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49813-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49813-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49813-218">CommonParameters</span></span>
<span data-ttu-id="49813-219">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49813-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49813-220">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49813-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49813-221">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49813-221">INPUTS</span></span>

### <span data-ttu-id="49813-222">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="49813-222">None</span></span>

## <span data-ttu-id="49813-223">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49813-223">OUTPUTS</span></span>

### <span data-ttu-id="49813-224">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="49813-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="49813-225">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49813-225">NOTES</span></span>

## <span data-ttu-id="49813-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49813-226">RELATED LINKS</span></span>
