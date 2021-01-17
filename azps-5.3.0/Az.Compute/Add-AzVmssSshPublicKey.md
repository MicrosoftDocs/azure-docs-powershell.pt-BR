---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430263"
---
# <span data-ttu-id="f1861-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f1861-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="f1861-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1861-102">SYNOPSIS</span></span>
<span data-ttu-id="f1861-103">Adiciona chaves públicas SSH ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1861-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="f1861-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1861-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1861-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1861-105">DESCRIPTION</span></span>
<span data-ttu-id="f1861-106">O cmdlet **Add-AzVmssSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar às máquinas virtuais do VMSS (conjunto de dimensionamento de máquina virtual) pelo Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="f1861-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="f1861-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1861-107">EXAMPLES</span></span>

### <span data-ttu-id="f1861-108">Exemplo 1: adicionar uma chave pública SSH ao VMSS</span><span class="sxs-lookup"><span data-stu-id="f1861-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="f1861-109">Este exemplo adiciona uma chave pública SSH ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1861-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="f1861-110">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1861-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="f1861-111">O segundo comando adiciona uma chave SSH com os dados de chave especificados e armazena a chave no caminho especificado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1861-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="f1861-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1861-112">PARAMETERS</span></span>

### <span data-ttu-id="f1861-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1861-113">-DefaultProfile</span></span>
<span data-ttu-id="f1861-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1861-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1861-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="f1861-115">-KeyData</span></span>
<span data-ttu-id="f1861-116">Especifica os dados de chave pública do SSH da RSA.</span><span class="sxs-lookup"><span data-stu-id="f1861-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="f1861-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f1861-117">-Path</span></span>
<span data-ttu-id="f1861-118">Especifica o caminho completo de um arquivo, na máquina virtual, em que esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="f1861-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="f1861-119">Se o arquivo já existir, esse cmdlet acrescentará a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1861-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1861-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f1861-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f1861-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1861-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="f1861-122">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="f1861-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1861-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1861-123">-Confirm</span></span>
<span data-ttu-id="f1861-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1861-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1861-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1861-125">-WhatIf</span></span>
<span data-ttu-id="f1861-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1861-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1861-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1861-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1861-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1861-128">CommonParameters</span></span>
<span data-ttu-id="f1861-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1861-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1861-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1861-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1861-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1861-131">INPUTS</span></span>

### <span data-ttu-id="f1861-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f1861-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f1861-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f1861-133">System.String</span></span>

## <span data-ttu-id="f1861-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1861-134">OUTPUTS</span></span>

### <span data-ttu-id="f1861-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f1861-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f1861-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1861-136">NOTES</span></span>

## <span data-ttu-id="f1861-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1861-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1861-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f1861-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
