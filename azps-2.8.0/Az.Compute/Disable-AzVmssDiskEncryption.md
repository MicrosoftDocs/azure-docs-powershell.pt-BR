---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 1b816e51d93ed375a8b281bba360a103380e9476
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597493"
---
# <span data-ttu-id="36157-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="36157-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="36157-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36157-102">SYNOPSIS</span></span>
<span data-ttu-id="36157-103">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="36157-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="36157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36157-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36157-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36157-105">DESCRIPTION</span></span>
<span data-ttu-id="36157-106">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="36157-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="36157-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36157-107">EXAMPLES</span></span>

### <span data-ttu-id="36157-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36157-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="36157-109">Desabilita a criptografia de disco no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="36157-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="36157-110">OS</span><span class="sxs-lookup"><span data-stu-id="36157-110">PARAMETERS</span></span>

### <span data-ttu-id="36157-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36157-111">-AsJob</span></span>
<span data-ttu-id="36157-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="36157-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36157-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36157-113">-DefaultProfile</span></span>
<span data-ttu-id="36157-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36157-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36157-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="36157-115">-ExtensionName</span></span>
<span data-ttu-id="36157-116">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="36157-116">The extension name.</span></span>
<span data-ttu-id="36157-117">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="36157-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36157-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36157-118">-Force</span></span>
<span data-ttu-id="36157-119">Para forçar a remoção da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36157-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="36157-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="36157-120">-ForceUpdate</span></span>
<span data-ttu-id="36157-121">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="36157-121">Generate a tag for force update.</span></span>  <span data-ttu-id="36157-122">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="36157-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36157-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36157-123">-ResourceGroupName</span></span>
<span data-ttu-id="36157-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36157-124">The resource group name.</span></span>

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

### <span data-ttu-id="36157-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36157-125">-VMScaleSetName</span></span>
<span data-ttu-id="36157-126">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36157-126">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36157-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="36157-127">-VolumeType</span></span>
<span data-ttu-id="36157-128">Tipo do volume (so ou dados) para executar a operação de criptografia</span><span class="sxs-lookup"><span data-stu-id="36157-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36157-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36157-129">-Confirm</span></span>
<span data-ttu-id="36157-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36157-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36157-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36157-131">-WhatIf</span></span>
<span data-ttu-id="36157-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36157-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36157-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36157-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36157-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36157-134">CommonParameters</span></span>
<span data-ttu-id="36157-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36157-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36157-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36157-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36157-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36157-137">INPUTS</span></span>

### <span data-ttu-id="36157-138">System. String</span><span class="sxs-lookup"><span data-stu-id="36157-138">System.String</span></span>

### <span data-ttu-id="36157-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36157-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36157-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36157-140">OUTPUTS</span></span>

### <span data-ttu-id="36157-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36157-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36157-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36157-142">NOTES</span></span>

## <span data-ttu-id="36157-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36157-143">RELATED LINKS</span></span>
