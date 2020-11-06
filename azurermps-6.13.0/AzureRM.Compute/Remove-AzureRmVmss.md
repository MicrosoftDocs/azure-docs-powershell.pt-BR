---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 54c6f9f399cfabf7a418939b4662c9bcfdc83d34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433296"
---
# <span data-ttu-id="4c936-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="4c936-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c936-102">SYNOPSIS</span></span>
<span data-ttu-id="4c936-103">Remove o VMSS ou uma máquina virtual que está dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c936-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c936-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c936-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c936-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c936-105">DESCRIPTION</span></span>
<span data-ttu-id="4c936-106">O cmdlet **Remove-AzureRmVmss** remove o VMSS (conjunto de escala da máquina virtual) do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c936-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="4c936-107">Esse cmdlet também pode ser usado para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c936-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="4c936-108">Você pode usar o parâmetro *InstanceId* para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c936-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="4c936-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c936-109">EXAMPLES</span></span>

### <span data-ttu-id="4c936-110">Exemplo 1: remover um VMSS</span><span class="sxs-lookup"><span data-stu-id="4c936-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="4c936-111">Esse comando Remove a VMSS chamada VMScaleSet001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="4c936-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="4c936-112">Exemplo 2: remover uma máquina virtual de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="4c936-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="4c936-113">Esse comando Remove a máquina virtual com a ID de instância 3 da VMSS chamada VMScaleSet002 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="4c936-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="4c936-114">OS</span><span class="sxs-lookup"><span data-stu-id="4c936-114">PARAMETERS</span></span>

### <span data-ttu-id="4c936-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c936-115">-AsJob</span></span>
<span data-ttu-id="4c936-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4c936-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4c936-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c936-117">-DefaultProfile</span></span>
<span data-ttu-id="4c936-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c936-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c936-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4c936-119">-Force</span></span>
<span data-ttu-id="4c936-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4c936-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c936-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4c936-121">-InstanceId</span></span>
<span data-ttu-id="4c936-122">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="4c936-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="4c936-123">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="4c936-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="4c936-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c936-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c936-125">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="4c936-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="4c936-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4c936-126">-VMScaleSetName</span></span>
<span data-ttu-id="4c936-127">Especifica o nome do VMSS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="4c936-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="4c936-128">Se você especificar o parâmetro *InstanceId* , o cmdlet removerá a máquina virtual especificada do VMSS nomeado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4c936-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="4c936-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c936-129">-Confirm</span></span>
<span data-ttu-id="4c936-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c936-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c936-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c936-131">-WhatIf</span></span>
<span data-ttu-id="4c936-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c936-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c936-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c936-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c936-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c936-134">CommonParameters</span></span>
<span data-ttu-id="4c936-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c936-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c936-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c936-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c936-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c936-137">INPUTS</span></span>

### <span data-ttu-id="4c936-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4c936-138">System.String</span></span>

### <span data-ttu-id="4c936-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="4c936-139">System.String[]</span></span>

## <span data-ttu-id="4c936-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c936-140">OUTPUTS</span></span>

### <span data-ttu-id="4c936-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4c936-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4c936-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c936-142">NOTES</span></span>

## <span data-ttu-id="4c936-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c936-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c936-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="4c936-145">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="4c936-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="4c936-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="4c936-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="4c936-149">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="4c936-150">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4c936-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


