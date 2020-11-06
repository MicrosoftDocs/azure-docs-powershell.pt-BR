---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603128"
---
# <span data-ttu-id="41f00-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="41f00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41f00-102">SYNOPSIS</span></span>
<span data-ttu-id="41f00-103">Inicia o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="41f00-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41f00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41f00-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f00-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41f00-105">DESCRIPTION</span></span>
<span data-ttu-id="41f00-106">O cmdlet **Start-AzureRmVmss** inicia todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="41f00-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="41f00-107">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="41f00-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="41f00-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41f00-108">EXAMPLES</span></span>

### <span data-ttu-id="41f00-109">Exemplo 1: iniciar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="41f00-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="41f00-110">Esse comando inicia um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertence à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="41f00-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="41f00-111">Exemplo 2: iniciar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="41f00-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="41f00-112">Esse comando inicia todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="41f00-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="41f00-113">OS</span><span class="sxs-lookup"><span data-stu-id="41f00-113">PARAMETERS</span></span>

### <span data-ttu-id="41f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f00-114">-DefaultProfile</span></span>
<span data-ttu-id="41f00-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41f00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f00-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="41f00-116">-InstanceId</span></span>
<span data-ttu-id="41f00-117">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="41f00-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="41f00-118">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="41f00-118">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f00-119">-ResourceGroupName</span></span>
<span data-ttu-id="41f00-120">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="41f00-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="41f00-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="41f00-121">-VMScaleSetName</span></span>
<span data-ttu-id="41f00-122">Especifica o nome do VMSS que este cmdlet inicia nas máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="41f00-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f00-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41f00-123">-Confirm</span></span>
<span data-ttu-id="41f00-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41f00-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f00-125">-WhatIf</span></span>
<span data-ttu-id="41f00-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41f00-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41f00-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41f00-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f00-128">CommonParameters</span></span>
<span data-ttu-id="41f00-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f00-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f00-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f00-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41f00-131">INPUTS</span></span>

## <span data-ttu-id="41f00-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41f00-132">OUTPUTS</span></span>

###  
<span data-ttu-id="41f00-133">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="41f00-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="41f00-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41f00-134">NOTES</span></span>

## <span data-ttu-id="41f00-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41f00-135">RELATED LINKS</span></span>

[<span data-ttu-id="41f00-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="41f00-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="41f00-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="41f00-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="41f00-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="41f00-141">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="41f00-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="41f00-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


