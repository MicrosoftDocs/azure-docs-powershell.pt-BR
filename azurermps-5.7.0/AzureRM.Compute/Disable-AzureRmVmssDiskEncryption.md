---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 7ff2512fa7c6247d75eb8b288c888dc2aff670dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430523"
---
# <span data-ttu-id="0f98c-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0f98c-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="0f98c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f98c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f98c-103">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="0f98c-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f98c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f98c-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f98c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f98c-105">DESCRIPTION</span></span>
<span data-ttu-id="0f98c-106">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="0f98c-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="0f98c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f98c-107">EXAMPLES</span></span>

### <span data-ttu-id="0f98c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f98c-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0f98c-109">Desabilita a criptografia de disco no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="0f98c-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0f98c-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f98c-110">PARAMETERS</span></span>

### <span data-ttu-id="0f98c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f98c-111">-AsJob</span></span>
<span data-ttu-id="0f98c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f98c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f98c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f98c-113">-DefaultProfile</span></span>
<span data-ttu-id="0f98c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f98c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f98c-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0f98c-115">-ExtensionName</span></span>
<span data-ttu-id="0f98c-116">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="0f98c-116">The extension name.</span></span>
<span data-ttu-id="0f98c-117">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="0f98c-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="0f98c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0f98c-118">-Force</span></span>
<span data-ttu-id="0f98c-119">Para forçar a remoção da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0f98c-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="0f98c-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="0f98c-120">-ForceUpdate</span></span>
<span data-ttu-id="0f98c-121">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="0f98c-121">Generate a tag for force update.</span></span>  <span data-ttu-id="0f98c-122">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="0f98c-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="0f98c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f98c-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f98c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f98c-124">The resource group name.</span></span>

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

### <span data-ttu-id="0f98c-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0f98c-125">-VMScaleSetName</span></span>
<span data-ttu-id="0f98c-126">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0f98c-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="0f98c-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="0f98c-127">-VolumeType</span></span>
<span data-ttu-id="0f98c-128">Tipo do volume (so ou dados) para executar a operação de criptografia</span><span class="sxs-lookup"><span data-stu-id="0f98c-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="0f98c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f98c-129">-Confirm</span></span>
<span data-ttu-id="0f98c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f98c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f98c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f98c-131">-WhatIf</span></span>
<span data-ttu-id="0f98c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f98c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f98c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f98c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f98c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f98c-134">CommonParameters</span></span>
<span data-ttu-id="0f98c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f98c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f98c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f98c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f98c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f98c-137">INPUTS</span></span>

### <span data-ttu-id="0f98c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0f98c-138">System.String</span></span>

## <span data-ttu-id="0f98c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f98c-139">OUTPUTS</span></span>

### <span data-ttu-id="0f98c-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0f98c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0f98c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f98c-141">NOTES</span></span>

## <span data-ttu-id="0f98c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f98c-142">RELATED LINKS</span></span>
