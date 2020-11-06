---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441179"
---
# <span data-ttu-id="0b5bf-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0b5bf-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="0b5bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5bf-103">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b5bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b5bf-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b5bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b5bf-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5bf-106">Desabilita a criptografia de disco em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="0b5bf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b5bf-107">EXAMPLES</span></span>

### <span data-ttu-id="0b5bf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b5bf-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0b5bf-109">Desabilita a criptografia de disco no conjunto de escala da VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0b5bf-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b5bf-110">PARAMETERS</span></span>

### <span data-ttu-id="0b5bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5bf-111">-DefaultProfile</span></span>
<span data-ttu-id="0b5bf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5bf-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0b5bf-113">-ExtensionName</span></span>
<span data-ttu-id="0b5bf-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-114">The extension name.</span></span>
<span data-ttu-id="0b5bf-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs do Windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="0b5bf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0b5bf-116">-Force</span></span>
<span data-ttu-id="0b5bf-117">Para forçar a remoção da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="0b5bf-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="0b5bf-118">-ForceUpdate</span></span>
<span data-ttu-id="0b5bf-119">Gerar uma marca para a atualização de força.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-119">Generate a tag for force update.</span></span>  <span data-ttu-id="0b5bf-120">Isso deve ser fornecido para executar operações de criptografia repetidas na mesma VM.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="0b5bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="0b5bf-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-122">The resource group name.</span></span>

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

### <span data-ttu-id="0b5bf-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0b5bf-123">-VMScaleSetName</span></span>
<span data-ttu-id="0b5bf-124">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="0b5bf-125">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="0b5bf-125">-VolumeType</span></span>
<span data-ttu-id="0b5bf-126">Tipo do volume (so ou dados) para executar a operação de criptografia</span><span class="sxs-lookup"><span data-stu-id="0b5bf-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="0b5bf-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b5bf-127">-Confirm</span></span>
<span data-ttu-id="0b5bf-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5bf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5bf-129">-WhatIf</span></span>
<span data-ttu-id="0b5bf-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b5bf-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5bf-132">CommonParameters</span></span>
<span data-ttu-id="0b5bf-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b5bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5bf-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5bf-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b5bf-135">INPUTS</span></span>

### <span data-ttu-id="0b5bf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b5bf-136">System.String</span></span>

## <span data-ttu-id="0b5bf-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b5bf-137">OUTPUTS</span></span>

### <span data-ttu-id="0b5bf-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0b5bf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0b5bf-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b5bf-139">NOTES</span></span>

## <span data-ttu-id="0b5bf-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b5bf-140">RELATED LINKS</span></span>

