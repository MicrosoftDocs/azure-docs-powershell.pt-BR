---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112152"
---
# <span data-ttu-id="884ae-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="884ae-101">Get-AzContainerService</span></span>

## <span data-ttu-id="884ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="884ae-102">SYNOPSIS</span></span>
<span data-ttu-id="884ae-103">Obtém um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="884ae-103">Gets a container service.</span></span>

## <span data-ttu-id="884ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="884ae-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884ae-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="884ae-105">DESCRIPTION</span></span>
<span data-ttu-id="884ae-106">O **cmdlet Get-AzContainerService** obtém um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="884ae-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="884ae-107">Você pode exibir as propriedades de um serviço de contêiner, que incluem estado, número de mestres e agentes e nome de domínio totalmente qualificado de mestre e agente.</span><span class="sxs-lookup"><span data-stu-id="884ae-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="884ae-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="884ae-108">EXAMPLES</span></span>

### <span data-ttu-id="884ae-109">Exemplo 1: Obter um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="884ae-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="884ae-110">Esse comando obtém um serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="884ae-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="884ae-111">Exemplo 2: Obter todos os serviços de contêineres</span><span class="sxs-lookup"><span data-stu-id="884ae-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="884ae-112">Este comando obtém todos os serviços de contêiner em assinatura.</span><span class="sxs-lookup"><span data-stu-id="884ae-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="884ae-113">Exemplo 3: Obter todos os serviços de contêiner no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="884ae-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="884ae-114">Esse comando obtém todos os serviços de contêiner no ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="884ae-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="884ae-115">Exemplo 4: Obter todos os serviços de contêiner usando filtro</span><span class="sxs-lookup"><span data-stu-id="884ae-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="884ae-116">Esse comando obtém todos os serviços de contêiner começando com "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="884ae-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="884ae-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="884ae-117">PARAMETERS</span></span>

### <span data-ttu-id="884ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884ae-118">-DefaultProfile</span></span>
<span data-ttu-id="884ae-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="884ae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="884ae-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="884ae-120">-Name</span></span>
<span data-ttu-id="884ae-121">Especifica o nome do serviço de contêiner que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="884ae-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="884ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="884ae-123">Especifica o grupo de recursos do serviço de contêineres que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="884ae-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="884ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884ae-124">CommonParameters</span></span>
<span data-ttu-id="884ae-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884ae-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884ae-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884ae-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="884ae-127">INPUTS</span></span>

### <span data-ttu-id="884ae-128">System.String</span><span class="sxs-lookup"><span data-stu-id="884ae-128">System.String</span></span>

## <span data-ttu-id="884ae-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="884ae-129">OUTPUTS</span></span>

### <span data-ttu-id="884ae-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="884ae-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="884ae-131">Notas</span><span class="sxs-lookup"><span data-stu-id="884ae-131">NOTES</span></span>

## <span data-ttu-id="884ae-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="884ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="884ae-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="884ae-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="884ae-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="884ae-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="884ae-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="884ae-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


