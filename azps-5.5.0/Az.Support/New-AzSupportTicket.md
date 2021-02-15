---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112422"
---
# <span data-ttu-id="12011-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="12011-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="12011-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12011-102">SYNOPSIS</span></span>
<span data-ttu-id="12011-103">Cria um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-103">Creates a support ticket.</span></span>

## <span data-ttu-id="12011-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12011-104">SYNTAX</span></span>

### <span data-ttu-id="12011-105">CreateSupportTicketWithContactDetailParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12011-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12011-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12011-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12011-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12011-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12011-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12011-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12011-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="12011-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12011-110">CriarQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="12011-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12011-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="12011-111">DESCRIPTION</span></span>
<span data-ttu-id="12011-112">Esse cmdlet pode ser usado para criar um tíquete de suporte para problemas de Cobrança, Gerenciamento de Assinatura, Cota ou Técnico.</span><span class="sxs-lookup"><span data-stu-id="12011-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="12011-113">Use Get-AzSupportService e Get-AzSupportProblemClassification cmdlets para identificar o serviço do Azure e as classificações de problemas correspondentes respectivamente para as quais você deseja solicitar suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="12011-114">Você deve especificar os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="12011-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="12011-115">Você pode usar New-AzSupportContactProfileObject cmdlet auxiliar para criar objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="12011-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="12011-116">Os Provedores de Soluções na Nuvem podem criar um tíquete de suporte para as assinaturas de seus clientes fazendo logon no locatário do cliente e especificando a ID do locatário local usando o parâmetro *CSPHomeTenantId.*</span><span class="sxs-lookup"><span data-stu-id="12011-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="12011-117">__Para tíquetes técnicos:__</span><span class="sxs-lookup"><span data-stu-id="12011-117">__For technical tickets:__</span></span>

<span data-ttu-id="12011-118">Para especificar o nome do recurso, especifique a ID de recurso ARM do recurso usando o parâmetro *TechnicalTicketResourceId.*</span><span class="sxs-lookup"><span data-stu-id="12011-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="12011-119">Veja um exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="12011-119">See an example below.</span></span> 

<span data-ttu-id="12011-120">__Para tíquetes de cota:__</span><span class="sxs-lookup"><span data-stu-id="12011-120">__For quota tickets:__</span></span>

<span data-ttu-id="12011-121">Para solicitar aumento de cota para **Compute VM Cores,** **Lote,** Banco de Dados **SQL** e **SQL Data Warehouse,** forneça detalhes adicionais no objeto *QuotaTicketDetail.*</span><span class="sxs-lookup"><span data-stu-id="12011-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="12011-122">O objeto QuotaTicketDetail consiste em 3 propriedades conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="12011-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="12011-123">Para uma documentação detalhada, [clique aqui.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="12011-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="12011-124">Para uma documentação detalhada sobre como construir o Payload para vários tipos de cota, [clique aqui](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="12011-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="12011-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12011-125">EXAMPLES</span></span>

### <span data-ttu-id="12011-126">Exemplo 1: Criar um tíquete de suporte de Gerenciamento de Assinatura ou Cobrança.</span><span class="sxs-lookup"><span data-stu-id="12011-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="12011-127">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de cobrança ou gerenciamento de assinatura para a qual você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="12011-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-128">Exemplo 2: Criar um tíquete de suporte técnico para o recurso Virtual Machine para Windows.</span><span class="sxs-lookup"><span data-stu-id="12011-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="12011-129">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do Computador Virtual para Windows para o qual você deseja solicitar suporte</span><span class="sxs-lookup"><span data-stu-id="12011-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-130">Exemplo 3: Criar um tíquete de suporte de cota para aumentar a cota de Núcleos de Máquina Virtuais para uma família VM específica.</span><span class="sxs-lookup"><span data-stu-id="12011-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="12011-131">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de VM Cores de Computação de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-132">Exemplo 4: Criar um tíquete de suporte de cota para aumentar a cota de núcleos de baixa prioridade para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="12011-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="12011-133">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-134">Exemplo 5: Crie um tíquete de suporte de cota para aumentar a cota de núcleos VM de uma Família VM específica para uma conta em lote.</span><span class="sxs-lookup"><span data-stu-id="12011-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="12011-135">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-136">Exemplo 6: Criar um tíquete de suporte de cota para aumentar a cota pools de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="12011-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="12011-137">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-138">Exemplo 7: Criar um tíquete de suporte de cota para aumentar a cota de trabalhos ativos e cronogramas de trabalho para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="12011-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="12011-139">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-140">Exemplo 8: Crie um tíquete de suporte de cota para aumentar o número de contas em lotes de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="12011-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="12011-141">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar GUIDs corretos para a classificação de problemas de Lote de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-142">Exemplo 9: Criar um tíquete de suporte de cota para aumentar a cota de DTUs para banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="12011-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="12011-143">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do banco de dados SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="12011-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-144">Exemplo 10: Criar um tíquete de suporte de cota para aumentar a cota de Servidores para Banco de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="12011-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="12011-145">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do banco de dados SQL de cota.</span><span class="sxs-lookup"><span data-stu-id="12011-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-146">Exemplo 11: Criar um tíquete de suporte de cota para aumentar a cota de DTUs para SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="12011-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="12011-147">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas de Data Warehouse do SQL cota.</span><span class="sxs-lookup"><span data-stu-id="12011-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-148">Exemplo 12: Criar um tíquete de suporte de cota para aumentar a cota para servidores do SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="12011-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="12011-149">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do Sql Data Warehouse de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-150">Exemplo 13: Criar um tíquete de suporte de cota para aumentar a cota de núcleos de baixa prioridade para o serviço de Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="12011-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="12011-151">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do serviço de Aprendizado de Máquina de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-152">Exemplo 14: Criar um tíquete de suporte de cota para aumentar a cota de núcleos VM para um serviço VM Family for Machine Learning específico.</span><span class="sxs-lookup"><span data-stu-id="12011-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="12011-153">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do serviço de Aprendizado de Máquina de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-154">Exemplo 15: Criar um tíquete de suporte de cota para aumentar a cota para a Instância Gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="12011-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="12011-155">Use Get-AzSupportService e Get-AzSupportProblemClassification para recuperar os GUIDs corretos para a classificação de problemas do serviço de Instância Gerenciada do SQL cota.</span><span class="sxs-lookup"><span data-stu-id="12011-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-156">Exemplo 16: crie um tíquete de suporte especificando parâmetros de contato do cliente individuais em vez do objeto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="12011-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-157">Exemplo 17: Crie um tíquete de suporte com solicitação de resposta 24 horas por dia, 7 dias por dia, no Azure.</span><span class="sxs-lookup"><span data-stu-id="12011-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12011-158">Exemplo 18: Crie um tíquete de suporte em nome do seu cliente se você for um Provedor de Soluções na Nuvem (CSP).</span><span class="sxs-lookup"><span data-stu-id="12011-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="12011-159">O CSP deve primeiro entrar em seu locatário e, em seguida, entrar no locatário do cliente, conforme mostrado no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="12011-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="12011-160">Em seguida, eles devem usar o parâmetro -CSPHomeTenantId para especificar sua ID de locatário página no momento da criação de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="12011-161">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12011-161">PARAMETERS</span></span>

### <span data-ttu-id="12011-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="12011-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="12011-163">Endereços de email adicionais.</span><span class="sxs-lookup"><span data-stu-id="12011-163">Additional email addresses.</span></span>
<span data-ttu-id="12011-164">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="12011-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12011-165">-AsJob</span></span>
<span data-ttu-id="12011-166">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="12011-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="12011-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="12011-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="12011-168">Esta é a ID de locatário página do usuário do Provedor de Soluções na Nuvem tentando criar um tíquete de suporte para o cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="12011-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="12011-169">-CustomerContactDetail</span></span>
<span data-ttu-id="12011-170">Detalhes de contato do cliente associados ao recurso SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="12011-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="12011-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="12011-171">-CustomerCountry</span></span>
<span data-ttu-id="12011-172">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-172">Customer country.</span></span>
<span data-ttu-id="12011-173">Esse deve ser um código de país ISO Alpha-3 válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="12011-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="12011-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="12011-174">-CustomerFirstName</span></span>
<span data-ttu-id="12011-175">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-175">Customer first name.</span></span>

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

### <span data-ttu-id="12011-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="12011-176">-CustomerLastName</span></span>
<span data-ttu-id="12011-177">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-177">Customer last name.</span></span>

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

### <span data-ttu-id="12011-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="12011-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="12011-179">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-179">Customer phone number.</span></span>
<span data-ttu-id="12011-180">Isso é necessário se o método de contato preferencial for telefone.</span><span class="sxs-lookup"><span data-stu-id="12011-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="12011-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="12011-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="12011-182">Idioma adiado do personalizado.</span><span class="sxs-lookup"><span data-stu-id="12011-182">Peferred language of the custom.</span></span>
<span data-ttu-id="12011-183">Esse deve ser um código de controle de idioma válido para um dos idiomas com suporte listados https://azure.microsoft.com/en-us/support/faq/ aqui.</span><span class="sxs-lookup"><span data-stu-id="12011-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="12011-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="12011-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="12011-185">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-185">Customer preferred time zone.</span></span>
<span data-ttu-id="12011-186">Esse deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="12011-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="12011-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="12011-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="12011-188">Endereço de email principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="12011-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="12011-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12011-189">-DefaultProfile</span></span>
<span data-ttu-id="12011-190">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12011-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12011-191">-Descrição</span><span class="sxs-lookup"><span data-stu-id="12011-191">-Description</span></span>
<span data-ttu-id="12011-192">Descrição detalhada da pergunta ou problema.</span><span class="sxs-lookup"><span data-stu-id="12011-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="12011-193">-Nome</span><span class="sxs-lookup"><span data-stu-id="12011-193">-Name</span></span>
<span data-ttu-id="12011-194">Nome do tíquete de suporte que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="12011-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="12011-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="12011-195">-PreferredContactMethod</span></span>
<span data-ttu-id="12011-196">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="12011-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="12011-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="12011-197">-ProblemClassificationId</span></span>
<span data-ttu-id="12011-198">Cada serviço do Azure tem seu próprio conjunto de categorias de problemas chamada classificação de problemas que corresponde ao tipo de problema que você está enfrentando.</span><span class="sxs-lookup"><span data-stu-id="12011-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="12011-199">Este parâmetro é a ID de recurso ARM do recurso ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="12011-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="12011-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="12011-200">-ProblemStartTime</span></span>
<span data-ttu-id="12011-201">Data e hora em que o problema começou.</span><span class="sxs-lookup"><span data-stu-id="12011-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="12011-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="12011-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="12011-203">Detalhes adicionais para um tíquete de suporte de Cota.</span><span class="sxs-lookup"><span data-stu-id="12011-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="12011-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="12011-204">-Require24X7Response</span></span>
<span data-ttu-id="12011-205">Indica se esse tíquete de suporte requer uma resposta 24 horas por dia, 7 dias por semana do Azure.</span><span class="sxs-lookup"><span data-stu-id="12011-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="12011-206">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="12011-206">-Severity</span></span>
<span data-ttu-id="12011-207">Gravidade do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-207">Severity of the support ticket.</span></span>
<span data-ttu-id="12011-208">Isso indica a urgência do caso, que, por sua vez, determina o tempo de resposta de acordo com o contrato de nível de serviço do plano de suporte técnico que você tem com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12011-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="12011-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="12011-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="12011-210">Esta é a ID de recurso do recurso de serviço do Azure (por exemplo: um recurso de máquina virtual ou um recurso HDInsight) para o qual o tíquete de suporte é criado.</span><span class="sxs-lookup"><span data-stu-id="12011-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="12011-211">-Título</span><span class="sxs-lookup"><span data-stu-id="12011-211">-Title</span></span>
<span data-ttu-id="12011-212">Título do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="12011-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="12011-213">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="12011-213">-Confirm</span></span>
<span data-ttu-id="12011-214">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12011-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12011-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12011-215">-WhatIf</span></span>
<span data-ttu-id="12011-216">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="12011-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12011-217">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12011-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12011-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12011-218">CommonParameters</span></span>
<span data-ttu-id="12011-219">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12011-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12011-220">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12011-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12011-221">Entradas</span><span class="sxs-lookup"><span data-stu-id="12011-221">INPUTS</span></span>

### <span data-ttu-id="12011-222">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12011-222">None</span></span>

## <span data-ttu-id="12011-223">Saídas</span><span class="sxs-lookup"><span data-stu-id="12011-223">OUTPUTS</span></span>

### <span data-ttu-id="12011-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="12011-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="12011-225">Notas</span><span class="sxs-lookup"><span data-stu-id="12011-225">NOTES</span></span>

## <span data-ttu-id="12011-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12011-226">RELATED LINKS</span></span>
