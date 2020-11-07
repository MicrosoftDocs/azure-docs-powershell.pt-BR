---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786187"
---
# <span data-ttu-id="04567-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="04567-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="04567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04567-102">SYNOPSIS</span></span>
<span data-ttu-id="04567-103">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="04567-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04567-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04567-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04567-105">DESCRIPTION</span></span>
<span data-ttu-id="04567-106">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="04567-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="04567-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04567-107">EXAMPLES</span></span>

### <span data-ttu-id="04567-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04567-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="04567-109">Desabilita a criptografia de disco no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="04567-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="04567-110">OS</span><span class="sxs-lookup"><span data-stu-id="04567-110">PARAMETERS</span></span>

### <span data-ttu-id="04567-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04567-111">-AsJob</span></span>
<span data-ttu-id="04567-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04567-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04567-113">-DefaultProfile</span></span>
<span data-ttu-id="04567-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04567-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04567-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="04567-115">-ExtensionName</span></span>
<span data-ttu-id="04567-116">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="04567-116">The extension name.</span></span>
<span data-ttu-id="04567-117">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="04567-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04567-118">-Force</span><span class="sxs-lookup"><span data-stu-id="04567-118">-Force</span></span>
<span data-ttu-id="04567-119">Para forçar a remoção da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04567-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="04567-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="04567-120">-ForceUpdate</span></span>
<span data-ttu-id="04567-121">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="04567-121">Generate a tag for force update.</span></span>  <span data-ttu-id="04567-122">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="04567-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04567-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04567-123">-ResourceGroupName</span></span>
<span data-ttu-id="04567-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04567-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04567-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="04567-125">-VMScaleSetName</span></span>
<span data-ttu-id="04567-126">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04567-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04567-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="04567-127">-VolumeType</span></span>
<span data-ttu-id="04567-128">Tipo do volume (so ou dados) para executar a operação de criptografia</span><span class="sxs-lookup"><span data-stu-id="04567-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04567-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04567-129">-Confirm</span></span>
<span data-ttu-id="04567-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04567-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04567-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04567-131">-WhatIf</span></span>
<span data-ttu-id="04567-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04567-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04567-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04567-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04567-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04567-134">CommonParameters</span></span>
<span data-ttu-id="04567-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04567-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04567-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04567-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04567-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04567-137">INPUTS</span></span>

### <span data-ttu-id="04567-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04567-138">System.String</span></span>

## <span data-ttu-id="04567-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04567-139">OUTPUTS</span></span>

### <span data-ttu-id="04567-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="04567-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="04567-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04567-141">NOTES</span></span>

## <span data-ttu-id="04567-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04567-142">RELATED LINKS</span></span>

