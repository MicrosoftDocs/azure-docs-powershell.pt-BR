---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 0d86d4e01c39170975901f5c9262bc2857883eec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887940"
---
# <span data-ttu-id="905a4-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="905a4-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="905a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905a4-102">SYNOPSIS</span></span>
<span data-ttu-id="905a4-103">Cria um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-103">Creates a support ticket.</span></span>

## <span data-ttu-id="905a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="905a4-104">SYNTAX</span></span>

### <span data-ttu-id="905a4-105">CreateSupportTicketWithContactDetailParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="905a4-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="905a4-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="905a4-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="905a4-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="905a4-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="905a4-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905a4-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="905a4-111">DESCRIPTION</span></span>
<span data-ttu-id="905a4-112">Esse cmdlet pode ser usado para criar um tíquete de suporte para cobrança, gerenciamento de assinatura, cota ou problemas técnicos.</span><span class="sxs-lookup"><span data-stu-id="905a4-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="905a4-113">Use Get-AzSupportService e Get-AzSupportProblemClassification cmdlets para identificar o serviço do Azure e suas classificações de problemas correspondentes respectivamente para as quais você deseja solicitar suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="905a4-114">Você deve especificar os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="905a4-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="905a4-115">Você pode usar New-AzSupportContactProfileObject cmdlet auxiliar para criar o objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="905a4-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="905a4-116">Os Provedores de Soluções na Nuvem podem criar um tíquete de suporte para assinaturas de seus clientes fazendo logon no locatário do cliente e especificando sua id de locatário ínteante usando o parâmetro *CSPHomeTenantId.*</span><span class="sxs-lookup"><span data-stu-id="905a4-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="905a4-117">__Para tíquetes técnicos:__</span><span class="sxs-lookup"><span data-stu-id="905a4-117">__For technical tickets:__</span></span>

<span data-ttu-id="905a4-118">Para especificar o nome do recurso, especifique ARM ID do recurso usando *o parâmetro TechnicalTicketResourceId.*</span><span class="sxs-lookup"><span data-stu-id="905a4-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="905a4-119">Veja um exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="905a4-119">See an example below.</span></span> 

<span data-ttu-id="905a4-120">__Para tíquetes de cota:__</span><span class="sxs-lookup"><span data-stu-id="905a4-120">__For quota tickets:__</span></span>

<span data-ttu-id="905a4-121">Para solicitar aumento de cota para **Compute VM Cores,** **Batch,** **SQL Database** e SQL **Data Warehouse,** forneça detalhes adicionais no *objeto QuotaTicketDetail.*</span><span class="sxs-lookup"><span data-stu-id="905a4-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="905a4-122">O objeto QuotaTicketDetail consiste em 3 propriedades conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="905a4-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="905a4-123">Para documentação detalhada, clique [aqui.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="905a4-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="905a4-124">Para uma documentação detalhada sobre como construir Carga para vários tipos de cota, [clique aqui](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="905a4-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="905a4-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="905a4-125">EXAMPLES</span></span>

### <span data-ttu-id="905a4-126">Exemplo 1: Criar um tíquete de suporte de Gerenciamento de Cobrança ou Gerenciamento de Assinatura.</span><span class="sxs-lookup"><span data-stu-id="905a4-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="905a4-127">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Cobrança ou Gerenciamento de Assinaturas para a qual você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="905a4-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-128">Exemplo 2: Criar um tíquete de suporte técnico para o recurso Máquina Virtual para Windows.</span><span class="sxs-lookup"><span data-stu-id="905a4-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="905a4-129">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas da Máquina Virtual para Windows para a qual você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="905a4-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-130">Exemplo 3: Crie um tíquete de suporte de cota para aumentar a cota de Núcleos de Máquina Virtual para uma família de VM específica.</span><span class="sxs-lookup"><span data-stu-id="905a4-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="905a4-131">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de VM Cores de Computação de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-132">Exemplo 4: Crie um tíquete de suporte de cota para aumentar a cota para núcleos de baixa prioridade para uma conta Batch.</span><span class="sxs-lookup"><span data-stu-id="905a4-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="905a4-133">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-134">Exemplo 5: Crie um tíquete de suporte de cota para aumentar a cota de núcleos de VM para uma família de VMs específica para uma conta batch.</span><span class="sxs-lookup"><span data-stu-id="905a4-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="905a4-135">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-136">Exemplo 6: Crie um tíquete de suporte de cota para aumentar a cota pools para uma conta Batch.</span><span class="sxs-lookup"><span data-stu-id="905a4-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="905a4-137">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-138">Exemplo 7: Crie um tíquete de suporte de cota para aumentar a cota de agendamentos de trabalhos e trabalhos ativos para uma conta Batch.</span><span class="sxs-lookup"><span data-stu-id="905a4-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="905a4-139">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-140">Exemplo 8: Crie um tíquete de suporte de cota para aumentar o número de contas em lotes para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="905a4-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="905a4-141">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-142">Exemplo 9: Crie um tíquete de suporte de cota para aumentar a cota de DTUs para SQL Database.</span><span class="sxs-lookup"><span data-stu-id="905a4-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="905a4-143">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="905a4-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-144">Exemplo 10: Crie um tíquete de suporte de cota para aumentar a cota para Servidores para SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="905a4-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="905a4-145">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="905a4-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-146">Exemplo 11: Crie um tíquete de suporte de cota para aumentar a cota de DTUs para SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="905a4-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="905a4-147">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="905a4-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-148">Exemplo 12: Crie um tíquete de suporte de cota para aumentar a cota para Servidores para SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="905a4-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="905a4-149">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="905a4-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-150">Exemplo 13: Crie um tíquete de suporte de cota para aumentar a cota para núcleos de baixa prioridade para o serviço de Aprendizado de Máquina.</span><span class="sxs-lookup"><span data-stu-id="905a4-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="905a4-151">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas do serviço de Aprendizado de Máquina de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-152">Exemplo 14: Crie um tíquete de suporte de cota para aumentar a cota de núcleos de VM para um serviço específico de Família de VMs para Aprendizado de Máquina.</span><span class="sxs-lookup"><span data-stu-id="905a4-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="905a4-153">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas do serviço de Aprendizado de Máquina de Cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-154">Exemplo 15: Criar um tíquete de suporte de cota para aumentar a cota para a instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="905a4-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="905a4-155">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de SQL de Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="905a4-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-156">Exemplo 16: Crie um tíquete de suporte especificando parâmetros individuais de contato do cliente em vez do objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="905a4-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-157">Exemplo 17: Crie um tíquete de suporte com solicitação para resposta 24 x 7 do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a4-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="905a4-158">Exemplo 18: Crie um tíquete de suporte em nome do seu cliente se você for um Provedor de Soluções na Nuvem (CSP).</span><span class="sxs-lookup"><span data-stu-id="905a4-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="905a4-159">O CSP deve primeiro fazer logon em seu locatário e, em seguida, entrar no locatário do cliente, conforme mostrado no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="905a4-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="905a4-160">Em seguida, eles devem usar o parâmetro -CSPHomeTenantId para especificar sua ID de locatário no momento da criação de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="905a4-161">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="905a4-161">PARAMETERS</span></span>

### <span data-ttu-id="905a4-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="905a4-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="905a4-163">Endereços de email adicionais.</span><span class="sxs-lookup"><span data-stu-id="905a4-163">Additional email addresses.</span></span>
<span data-ttu-id="905a4-164">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="905a4-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="905a4-165">-AsJob</span></span>
<span data-ttu-id="905a4-166">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="905a4-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="905a4-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="905a4-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="905a4-168">Esta é a ID do locatário 1 do usuário do Provedor de Soluções na Nuvem tentando criar um tíquete de suporte para seu cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="905a4-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="905a4-169">-CustomerContactDetail</span></span>
<span data-ttu-id="905a4-170">Detalhes de contato do cliente associados ao recurso SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="905a4-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="905a4-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="905a4-171">-CustomerCountry</span></span>
<span data-ttu-id="905a4-172">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-172">Customer country.</span></span>
<span data-ttu-id="905a4-173">Este deve ser um código de país ISO Alpha-3 válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="905a4-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="905a4-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="905a4-174">-CustomerFirstName</span></span>
<span data-ttu-id="905a4-175">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-175">Customer first name.</span></span>

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

### <span data-ttu-id="905a4-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="905a4-176">-CustomerLastName</span></span>
<span data-ttu-id="905a4-177">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-177">Customer last name.</span></span>

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

### <span data-ttu-id="905a4-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="905a4-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="905a4-179">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-179">Customer phone number.</span></span>
<span data-ttu-id="905a4-180">Isso é necessário se o método de contato preferencial for telefone.</span><span class="sxs-lookup"><span data-stu-id="905a4-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="905a4-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="905a4-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="905a4-182">Idioma adiado do personalizado.</span><span class="sxs-lookup"><span data-stu-id="905a4-182">Peferred language of the custom.</span></span>
<span data-ttu-id="905a4-183">Esse deve ser um código de idioma válido para um dos idiomas com suporte listados aqui https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="905a4-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="905a4-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="905a4-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="905a4-185">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-185">Customer preferred time zone.</span></span>
<span data-ttu-id="905a4-186">Esse deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="905a4-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="905a4-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="905a4-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="905a4-188">Endereço de email principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="905a4-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="905a4-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905a4-189">-DefaultProfile</span></span>
<span data-ttu-id="905a4-190">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="905a4-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905a4-191">-Description</span><span class="sxs-lookup"><span data-stu-id="905a4-191">-Description</span></span>
<span data-ttu-id="905a4-192">Descrição detalhada da questão ou problema.</span><span class="sxs-lookup"><span data-stu-id="905a4-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="905a4-193">-Name</span><span class="sxs-lookup"><span data-stu-id="905a4-193">-Name</span></span>
<span data-ttu-id="905a4-194">Nome do tíquete de suporte que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="905a4-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="905a4-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="905a4-195">-PreferredContactMethod</span></span>
<span data-ttu-id="905a4-196">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="905a4-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="905a4-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="905a4-197">-ProblemClassificationId</span></span>
<span data-ttu-id="905a4-198">Cada serviço do Azure tem seu próprio conjunto de categorias de problemas chamada classificação de problemas que corresponde ao tipo de problema que você está enfrentando.</span><span class="sxs-lookup"><span data-stu-id="905a4-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="905a4-199">Este parâmetro é a ARM de recurso do recurso ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="905a4-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="905a4-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="905a4-200">-ProblemStartTime</span></span>
<span data-ttu-id="905a4-201">Data e hora em que o problema começou.</span><span class="sxs-lookup"><span data-stu-id="905a4-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="905a4-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="905a4-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="905a4-203">Detalhes adicionais para um tíquete de suporte de cota.</span><span class="sxs-lookup"><span data-stu-id="905a4-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="905a4-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="905a4-204">-Require24X7Response</span></span>
<span data-ttu-id="905a4-205">Indica se esse tíquete de suporte requer uma resposta 24x7 do Azure.</span><span class="sxs-lookup"><span data-stu-id="905a4-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="905a4-206">-Severity</span><span class="sxs-lookup"><span data-stu-id="905a4-206">-Severity</span></span>
<span data-ttu-id="905a4-207">Gravidade do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-207">Severity of the support ticket.</span></span>
<span data-ttu-id="905a4-208">Isso indica a urgência do caso, que, por sua vez, determina o tempo de resposta de acordo com o contrato de nível de serviço do plano de suporte técnico que você tem com o Azure.</span><span class="sxs-lookup"><span data-stu-id="905a4-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="905a4-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="905a4-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="905a4-210">Essa é a id de recurso do recurso de serviço do Azure (por exemplo: um recurso de máquina virtual ou um recurso HDInsight) para o qual o tíquete de suporte é criado.</span><span class="sxs-lookup"><span data-stu-id="905a4-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="905a4-211">-Title</span><span class="sxs-lookup"><span data-stu-id="905a4-211">-Title</span></span>
<span data-ttu-id="905a4-212">Título do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="905a4-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="905a4-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="905a4-213">-Confirm</span></span>
<span data-ttu-id="905a4-214">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="905a4-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905a4-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905a4-215">-WhatIf</span></span>
<span data-ttu-id="905a4-216">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="905a4-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905a4-217">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="905a4-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905a4-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905a4-218">CommonParameters</span></span>
<span data-ttu-id="905a4-219">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905a4-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905a4-220">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="905a4-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905a4-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="905a4-221">INPUTS</span></span>

### <span data-ttu-id="905a4-222">Nenhum</span><span class="sxs-lookup"><span data-stu-id="905a4-222">None</span></span>

## <span data-ttu-id="905a4-223">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="905a4-223">OUTPUTS</span></span>

### <span data-ttu-id="905a4-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="905a4-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="905a4-225">NOTES</span><span class="sxs-lookup"><span data-stu-id="905a4-225">NOTES</span></span>

## <span data-ttu-id="905a4-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="905a4-226">RELATED LINKS</span></span>
