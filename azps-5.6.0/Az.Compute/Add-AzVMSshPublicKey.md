---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889025"
---
# <span data-ttu-id="2766a-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2766a-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="2766a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2766a-102">SYNOPSIS</span></span>
<span data-ttu-id="2766a-103">Adiciona as chaves públicas para SSH para uma máquina virtual, ao criar apenas a VM.</span><span class="sxs-lookup"><span data-stu-id="2766a-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="2766a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2766a-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2766a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2766a-105">DESCRIPTION</span></span>
<span data-ttu-id="2766a-106">O cmdlet **Add-AzVMSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar a uma máquina virtual Linux por meio do Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="2766a-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="2766a-107">Isso não pode ser usado após a criação da VM, se você tentar usá-lo após a criação da VM sem o Update-AzVM, não haverá nenhum erro, se você usar o comando com Update-AzVM, o comando irá erro.</span><span class="sxs-lookup"><span data-stu-id="2766a-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="2766a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2766a-108">EXAMPLES</span></span>

### <span data-ttu-id="2766a-109">Exemplo 1: Adicionar uma chave pública a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="2766a-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="2766a-110">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="2766a-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="2766a-111">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2766a-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2766a-112">O segundo comando adiciona a chave pública ao local em VirtualMachine07 especificado pelo parâmetro Path.</span><span class="sxs-lookup"><span data-stu-id="2766a-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="2766a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2766a-113">PARAMETERS</span></span>

### <span data-ttu-id="2766a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2766a-114">-DefaultProfile</span></span>
<span data-ttu-id="2766a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2766a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2766a-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="2766a-116">-KeyData</span></span>
<span data-ttu-id="2766a-117">Especifica uma codificação base 64 de uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="2766a-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="2766a-118">Você pode se conectar a uma máquina virtual Linux usando SSH ou usando a chave especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2766a-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="2766a-119">-Path</span><span class="sxs-lookup"><span data-stu-id="2766a-119">-Path</span></span>
<span data-ttu-id="2766a-120">Especifica o caminho completo de um arquivo, na máquina virtual, onde esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="2766a-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="2766a-121">Se o arquivo já existir, esse cmdlet anexa a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="2766a-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="2766a-122">-VM</span><span class="sxs-lookup"><span data-stu-id="2766a-122">-VM</span></span>
<span data-ttu-id="2766a-123">Especifica o objeto de máquina virtual que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2766a-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="2766a-124">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="2766a-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="2766a-125">Você pode usar o cmdlet [New-AzVMConfig](./New-AzVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2766a-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2766a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2766a-126">CommonParameters</span></span>
<span data-ttu-id="2766a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2766a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2766a-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2766a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2766a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2766a-129">INPUTS</span></span>

### <span data-ttu-id="2766a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2766a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2766a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2766a-131">System.String</span></span>

## <span data-ttu-id="2766a-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2766a-132">OUTPUTS</span></span>

### <span data-ttu-id="2766a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2766a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2766a-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="2766a-134">NOTES</span></span>

## <span data-ttu-id="2766a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2766a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2766a-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2766a-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2766a-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2766a-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
