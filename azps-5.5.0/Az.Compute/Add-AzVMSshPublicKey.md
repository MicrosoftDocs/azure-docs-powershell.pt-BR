---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116555"
---
# <span data-ttu-id="ede9b-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ede9b-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="ede9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ede9b-102">SYNOPSIS</span></span>
<span data-ttu-id="ede9b-103">Adiciona as chaves públicas para SSH para uma máquina virtual, ao criar apenas o VM.</span><span class="sxs-lookup"><span data-stu-id="ede9b-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="ede9b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ede9b-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ede9b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ede9b-105">DESCRIPTION</span></span>
<span data-ttu-id="ede9b-106">O cmdlet **Add-AzVMSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar a uma máquina virtual do Linux por meio do Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="ede9b-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="ede9b-107">Isso não pode ser usado após a criação de VM, se você tentar usá-lo após a criação de VM sem o Update-AzVM, não haverá nenhum erro, se você usar o comando com Update-AzVM, o comando irá erro.</span><span class="sxs-lookup"><span data-stu-id="ede9b-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="ede9b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ede9b-108">EXAMPLES</span></span>

### <span data-ttu-id="ede9b-109">Exemplo 1: Adicionar uma chave pública a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ede9b-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="ede9b-110">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="ede9b-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="ede9b-111">O comando armazena a máquina virtual na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="ede9b-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ede9b-112">O segundo comando adiciona a chave pública ao local no VirtualMachine07 especificado pelo parâmetro Caminho.</span><span class="sxs-lookup"><span data-stu-id="ede9b-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="ede9b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ede9b-113">PARAMETERS</span></span>

### <span data-ttu-id="ede9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede9b-114">-DefaultProfile</span></span>
<span data-ttu-id="ede9b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ede9b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ede9b-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="ede9b-116">-KeyData</span></span>
<span data-ttu-id="ede9b-117">Especifica uma codificação de base 64 de uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="ede9b-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="ede9b-118">Você pode se conectar a uma máquina virtual do Linux usando SSH ou usando a chave especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ede9b-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="ede9b-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ede9b-119">-Path</span></span>
<span data-ttu-id="ede9b-120">Especifica o caminho completo de um arquivo, na máquina virtual, onde esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="ede9b-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="ede9b-121">Se o arquivo já existir, esse cmdlet anexa a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="ede9b-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="ede9b-122">-VM</span><span class="sxs-lookup"><span data-stu-id="ede9b-122">-VM</span></span>
<span data-ttu-id="ede9b-123">Especifica o objeto de máquina virtual que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ede9b-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="ede9b-124">Para obter um objeto de máquina virtual, use [o cmdlet Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="ede9b-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="ede9b-125">Você pode usar o [cmdlet New-AzVMConfig](./New-AzVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ede9b-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="ede9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede9b-126">CommonParameters</span></span>
<span data-ttu-id="ede9b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede9b-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ede9b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede9b-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="ede9b-129">INPUTS</span></span>

### <span data-ttu-id="ede9b-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ede9b-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ede9b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ede9b-131">System.String</span></span>

## <span data-ttu-id="ede9b-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="ede9b-132">OUTPUTS</span></span>

### <span data-ttu-id="ede9b-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ede9b-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ede9b-134">Notas</span><span class="sxs-lookup"><span data-stu-id="ede9b-134">NOTES</span></span>

## <span data-ttu-id="ede9b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ede9b-135">RELATED LINKS</span></span>

[<span data-ttu-id="ede9b-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ede9b-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ede9b-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ede9b-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
