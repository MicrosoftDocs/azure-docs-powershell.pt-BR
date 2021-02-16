---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117873"
---
# <span data-ttu-id="eb287-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="eb287-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="eb287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb287-102">SYNOPSIS</span></span>
<span data-ttu-id="eb287-103">Adiciona chaves públicas SSH ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb287-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="eb287-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb287-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb287-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb287-105">DESCRIPTION</span></span>
<span data-ttu-id="eb287-106">O cmdlet **Add-AzVmssSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar às máquinas virtuais VMSS (Virtual Machine Scale Set) por meio do Shell Seguro (SSH).</span><span class="sxs-lookup"><span data-stu-id="eb287-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="eb287-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb287-107">EXAMPLES</span></span>

### <span data-ttu-id="eb287-108">Exemplo 1: Adicionar uma chave pública SSH ao VMSS</span><span class="sxs-lookup"><span data-stu-id="eb287-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="eb287-109">Este exemplo adiciona uma chave pública SSH ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb287-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="eb287-110">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb287-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="eb287-111">O segundo comando adiciona uma tecla SSH com os dados de chave especificados e armazena a chave no caminho especificado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="eb287-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="eb287-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb287-112">PARAMETERS</span></span>

### <span data-ttu-id="eb287-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb287-113">-DefaultProfile</span></span>
<span data-ttu-id="eb287-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eb287-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb287-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="eb287-115">-KeyData</span></span>
<span data-ttu-id="eb287-116">Especifica dados de chave pública SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="eb287-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="eb287-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="eb287-117">-Path</span></span>
<span data-ttu-id="eb287-118">Especifica o caminho completo de um arquivo, na máquina virtual, onde esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="eb287-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="eb287-119">Se o arquivo já existir, esse cmdlet anexa a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb287-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="eb287-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb287-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="eb287-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb287-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="eb287-122">Você pode usar [o cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="eb287-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="eb287-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eb287-123">-Confirm</span></span>
<span data-ttu-id="eb287-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb287-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb287-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb287-125">-WhatIf</span></span>
<span data-ttu-id="eb287-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eb287-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb287-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb287-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb287-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb287-128">CommonParameters</span></span>
<span data-ttu-id="eb287-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb287-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb287-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb287-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb287-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="eb287-131">INPUTS</span></span>

### <span data-ttu-id="eb287-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb287-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="eb287-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eb287-133">System.String</span></span>

## <span data-ttu-id="eb287-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="eb287-134">OUTPUTS</span></span>

### <span data-ttu-id="eb287-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb287-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="eb287-136">Notas</span><span class="sxs-lookup"><span data-stu-id="eb287-136">NOTES</span></span>

## <span data-ttu-id="eb287-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb287-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb287-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="eb287-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
