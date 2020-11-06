---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: ff337ae0f5d0da86b035905bf83d2719edf1f4f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426803"
---
# <span data-ttu-id="82c04-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="82c04-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="82c04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82c04-102">SYNOPSIS</span></span>
<span data-ttu-id="82c04-103">Cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c04-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82c04-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82c04-105">DESCRIPTION</span></span>
<span data-ttu-id="82c04-106">O cmdlet **New-AzureRmContainerService** cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c04-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="82c04-107">Especifique um objeto de serviço de contêiner que você possa criar usando o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="82c04-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="82c04-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82c04-108">EXAMPLES</span></span>

### <span data-ttu-id="82c04-109">Exemplo 1: criar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="82c04-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="82c04-110">O primeiro comando cria um grupo de recursos chamado ResourceGroup17 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="82c04-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="82c04-111">Para obter mais informações, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="82c04-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="82c04-112">O segundo comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="82c04-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="82c04-113">Para obter mais informações, consulte o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="82c04-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="82c04-114">O comando final cria um serviço de contêiner para o contêiner armazenado em $Container.</span><span class="sxs-lookup"><span data-stu-id="82c04-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="82c04-115">O serviço é chamado csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="82c04-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="82c04-116">OS</span><span class="sxs-lookup"><span data-stu-id="82c04-116">PARAMETERS</span></span>

### <span data-ttu-id="82c04-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="82c04-117">-ContainerService</span></span>
<span data-ttu-id="82c04-118">Especifica um objeto de serviço de contêiner que contém as propriedades do novo serviço.</span><span class="sxs-lookup"><span data-stu-id="82c04-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="82c04-119">Para obter um objeto **ContainerService** , use o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="82c04-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82c04-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="82c04-120">-Name</span></span>
<span data-ttu-id="82c04-121">Especifica o nome do serviço de contêiner que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="82c04-121">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c04-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c04-122">-ResourceGroupName</span></span>
<span data-ttu-id="82c04-123">Especifica o grupo de recursos no qual esse cmdlet implanta o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c04-123">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c04-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82c04-124">-Confirm</span></span>
<span data-ttu-id="82c04-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c04-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c04-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c04-126">-WhatIf</span></span>
<span data-ttu-id="82c04-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82c04-127">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="82c04-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82c04-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c04-129">CommonParameters</span></span>
<span data-ttu-id="82c04-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c04-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c04-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c04-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82c04-132">INPUTS</span></span>

### <span data-ttu-id="82c04-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="82c04-133">None</span></span>
<span data-ttu-id="82c04-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="82c04-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82c04-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82c04-135">OUTPUTS</span></span>

## <span data-ttu-id="82c04-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82c04-136">NOTES</span></span>

## <span data-ttu-id="82c04-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82c04-137">RELATED LINKS</span></span>

[<span data-ttu-id="82c04-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="82c04-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="82c04-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="82c04-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="82c04-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="82c04-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="82c04-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="82c04-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


