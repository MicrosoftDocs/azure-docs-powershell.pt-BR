---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: d3677191bb3a196b97dcb8ff6c5b62b4aafd3a8b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775960"
---
# <span data-ttu-id="667bd-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-101">Start-AzVmss</span></span>

## <span data-ttu-id="667bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="667bd-102">SYNOPSIS</span></span>
<span data-ttu-id="667bd-103">Inicia o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="667bd-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="667bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="667bd-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="667bd-105">DESCRIPTION</span></span>
<span data-ttu-id="667bd-106">O cmdlet **Start-AzVmss** inicia todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="667bd-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="667bd-107">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="667bd-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="667bd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="667bd-108">EXAMPLES</span></span>

### <span data-ttu-id="667bd-109">Exemplo 1: iniciar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="667bd-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="667bd-110">Esse comando inicia um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertence à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="667bd-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="667bd-111">Exemplo 2: iniciar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="667bd-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="667bd-112">Esse comando inicia todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="667bd-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="667bd-113">OS</span><span class="sxs-lookup"><span data-stu-id="667bd-113">PARAMETERS</span></span>

### <span data-ttu-id="667bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667bd-114">-AsJob</span></span>
<span data-ttu-id="667bd-115">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="667bd-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="667bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667bd-116">-DefaultProfile</span></span>
<span data-ttu-id="667bd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="667bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667bd-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="667bd-118">-InstanceId</span></span>
<span data-ttu-id="667bd-119">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="667bd-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="667bd-120">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="667bd-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="667bd-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="667bd-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="667bd-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="667bd-123">-VMScaleSetName</span></span>
<span data-ttu-id="667bd-124">Especifica o nome do VMSS que este cmdlet inicia nas máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="667bd-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667bd-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="667bd-125">-Confirm</span></span>
<span data-ttu-id="667bd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="667bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667bd-127">-WhatIf</span></span>
<span data-ttu-id="667bd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="667bd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="667bd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="667bd-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667bd-130">CommonParameters</span></span>
<span data-ttu-id="667bd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667bd-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667bd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667bd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="667bd-133">INPUTS</span></span>

### <span data-ttu-id="667bd-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="667bd-134">None</span></span>
<span data-ttu-id="667bd-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="667bd-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="667bd-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="667bd-136">OUTPUTS</span></span>

###  
<span data-ttu-id="667bd-137">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="667bd-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="667bd-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="667bd-138">NOTES</span></span>

## <span data-ttu-id="667bd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="667bd-139">RELATED LINKS</span></span>

[<span data-ttu-id="667bd-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="667bd-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="667bd-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="667bd-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="667bd-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="667bd-145">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="667bd-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="667bd-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


