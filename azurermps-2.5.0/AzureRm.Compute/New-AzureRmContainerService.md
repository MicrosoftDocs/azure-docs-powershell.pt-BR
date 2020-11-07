---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785370"
---
# <span data-ttu-id="6b04d-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="6b04d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b04d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b04d-103">Cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6b04d-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b04d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b04d-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b04d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b04d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b04d-106">O cmdlet **New-AzureRmContainerService** cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6b04d-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="6b04d-107">Especifique um objeto de serviço de contêiner que você possa criar usando o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b04d-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="6b04d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b04d-108">EXAMPLES</span></span>

### <span data-ttu-id="6b04d-109">Exemplo 1: criar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="6b04d-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="6b04d-110">O primeiro comando cria um grupo de recursos chamado ResourceGroup17 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="6b04d-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="6b04d-111">Para obter mais informações, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6b04d-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="6b04d-112">O segundo comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="6b04d-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6b04d-113">Para obter mais informações, consulte o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b04d-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="6b04d-114">O comando final cria um serviço de contêiner para o contêiner armazenado em $Container.</span><span class="sxs-lookup"><span data-stu-id="6b04d-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="6b04d-115">O serviço é chamado csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="6b04d-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="6b04d-116">OS</span><span class="sxs-lookup"><span data-stu-id="6b04d-116">PARAMETERS</span></span>

### <span data-ttu-id="6b04d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b04d-117">-AsJob</span></span>
<span data-ttu-id="6b04d-118">RRun cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6b04d-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b04d-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-119">-ContainerService</span></span>
<span data-ttu-id="6b04d-120">Especifica um objeto de serviço de contêiner que contém as propriedades do novo serviço.</span><span class="sxs-lookup"><span data-stu-id="6b04d-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="6b04d-121">Para obter um objeto **ContainerService** , use o cmdlet New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="6b04d-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b04d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b04d-122">-DefaultProfile</span></span>
<span data-ttu-id="6b04d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b04d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b04d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b04d-124">-Name</span></span>
<span data-ttu-id="6b04d-125">Especifica o nome do serviço de contêiner que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="6b04d-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6b04d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b04d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b04d-127">Especifica o grupo de recursos no qual esse cmdlet implanta o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="6b04d-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="6b04d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b04d-128">-Confirm</span></span>
<span data-ttu-id="6b04d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b04d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b04d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b04d-130">-WhatIf</span></span>
<span data-ttu-id="6b04d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b04d-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6b04d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b04d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b04d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b04d-133">CommonParameters</span></span>
<span data-ttu-id="6b04d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b04d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b04d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b04d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b04d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b04d-136">INPUTS</span></span>

### <span data-ttu-id="6b04d-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-137">ContainerService</span></span>
<span data-ttu-id="6b04d-138">O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6b04d-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="6b04d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b04d-139">OUTPUTS</span></span>

### <span data-ttu-id="6b04d-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="6b04d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b04d-141">NOTES</span></span>

## <span data-ttu-id="6b04d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b04d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b04d-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="6b04d-144">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6b04d-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="6b04d-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="6b04d-146">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b04d-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


