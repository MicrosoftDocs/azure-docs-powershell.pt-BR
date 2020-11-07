---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: cd988a78962e1603be42e867fbc27bd0e58ff69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771184"
---
# <span data-ttu-id="5ff49-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-101">New-AzContainerService</span></span>

## <span data-ttu-id="5ff49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ff49-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff49-103">Cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ff49-103">Creates a container service.</span></span>

## <span data-ttu-id="5ff49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ff49-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ff49-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff49-106">O cmdlet **New-AzContainerService** cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ff49-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="5ff49-107">Especifique um objeto de serviço de contêiner que você possa criar usando o cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="5ff49-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="5ff49-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ff49-108">EXAMPLES</span></span>

### <span data-ttu-id="5ff49-109">Exemplo 1: criar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="5ff49-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="5ff49-110">O primeiro comando cria um grupo de recursos chamado ResourceGroup17 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="5ff49-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="5ff49-111">Para obter mais informações, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ff49-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="5ff49-112">O segundo comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="5ff49-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5ff49-113">Para obter mais informações, consulte o cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="5ff49-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="5ff49-114">O comando final cria um serviço de contêiner para o contêiner armazenado em $Container.</span><span class="sxs-lookup"><span data-stu-id="5ff49-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="5ff49-115">O serviço é chamado csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="5ff49-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="5ff49-116">OS</span><span class="sxs-lookup"><span data-stu-id="5ff49-116">PARAMETERS</span></span>

### <span data-ttu-id="5ff49-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff49-117">-AsJob</span></span>
<span data-ttu-id="5ff49-118">RRun cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5ff49-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5ff49-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-119">-ContainerService</span></span>
<span data-ttu-id="5ff49-120">Especifica um objeto de serviço de contêiner que contém as propriedades do novo serviço.</span><span class="sxs-lookup"><span data-stu-id="5ff49-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="5ff49-121">Para obter um objeto **ContainerService** , use o cmdlet New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="5ff49-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff49-122">-DefaultProfile</span></span>
<span data-ttu-id="5ff49-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ff49-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ff49-124">-Name</span></span>
<span data-ttu-id="5ff49-125">Especifica o nome do serviço de contêiner que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="5ff49-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff49-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ff49-127">Especifica o grupo de recursos no qual esse cmdlet implanta o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ff49-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff49-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ff49-128">-Confirm</span></span>
<span data-ttu-id="5ff49-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff49-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff49-130">-WhatIf</span></span>
<span data-ttu-id="5ff49-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ff49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff49-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ff49-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff49-133">CommonParameters</span></span>
<span data-ttu-id="5ff49-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff49-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff49-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ff49-136">INPUTS</span></span>

### <span data-ttu-id="5ff49-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff49-137">System.String</span></span>

### <span data-ttu-id="5ff49-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5ff49-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ff49-139">OUTPUTS</span></span>

### <span data-ttu-id="5ff49-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5ff49-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ff49-141">NOTES</span></span>

## <span data-ttu-id="5ff49-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ff49-142">RELATED LINKS</span></span>

[<span data-ttu-id="5ff49-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="5ff49-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="5ff49-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="5ff49-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="5ff49-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff49-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


