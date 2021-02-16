---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: af03fa8e29ab5912fb3e2d1809c9e2fc67941fb5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118557"
---
# <span data-ttu-id="8effe-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="8effe-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="8effe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8effe-102">SYNOPSIS</span></span>
<span data-ttu-id="8effe-103">Obter classificações de problemas para o serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="8effe-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="8effe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8effe-104">SYNTAX</span></span>

### <span data-ttu-id="8effe-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8effe-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8effe-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8effe-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8effe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8effe-107">DESCRIPTION</span></span>
<span data-ttu-id="8effe-108">Obtém a lista atual de classificação de problemas para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="8effe-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="8effe-109">Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando o New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8effe-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="8effe-110">Sempre use os GUIDs de classificação de problemas e serviço obtidos programaticamente.</span><span class="sxs-lookup"><span data-stu-id="8effe-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="8effe-111">Essa prática garante que você tenha os GUIDs de classificação de problemas e de serviço mais recentes para criação de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="8effe-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="8effe-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8effe-112">EXAMPLES</span></span>

### <span data-ttu-id="8effe-113">Exemplo 1: obter classificações de problemas para um serviço usando o parâmetro ID do serviço.</span><span class="sxs-lookup"><span data-stu-id="8effe-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="8effe-114">Exemplo 2: obter classificações de problemas para um serviço usando o objeto de serviço pai</span><span class="sxs-lookup"><span data-stu-id="8effe-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="8effe-115">Exemplo 3: Obter detalhes de um único problema classificaiton por id por objeto de serviço de piping</span><span class="sxs-lookup"><span data-stu-id="8effe-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="8effe-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8effe-116">PARAMETERS</span></span>

### <span data-ttu-id="8effe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8effe-117">-DefaultProfile</span></span>
<span data-ttu-id="8effe-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8effe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8effe-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8effe-119">-Id</span></span>
<span data-ttu-id="8effe-120">ID de classificação do problema.</span><span class="sxs-lookup"><span data-stu-id="8effe-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8effe-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="8effe-121">-ServiceId</span></span>
<span data-ttu-id="8effe-122">ID do serviço para a qual todas as classificações de problemas são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8effe-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8effe-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="8effe-123">-ServiceObject</span></span>
<span data-ttu-id="8effe-124">Objeto de serviço para o qual as classificações de problema são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8effe-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8effe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8effe-125">CommonParameters</span></span>
<span data-ttu-id="8effe-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8effe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8effe-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8effe-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8effe-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="8effe-128">INPUTS</span></span>

### <span data-ttu-id="8effe-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="8effe-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="8effe-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="8effe-130">OUTPUTS</span></span>

### <span data-ttu-id="8effe-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="8effe-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="8effe-132">Notas</span><span class="sxs-lookup"><span data-stu-id="8effe-132">NOTES</span></span>

## <span data-ttu-id="8effe-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8effe-133">RELATED LINKS</span></span>
