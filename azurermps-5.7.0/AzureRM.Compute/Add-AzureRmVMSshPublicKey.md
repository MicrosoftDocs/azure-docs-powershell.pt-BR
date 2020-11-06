---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602387"
---
# <span data-ttu-id="67173-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="67173-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="67173-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67173-102">SYNOPSIS</span></span>
<span data-ttu-id="67173-103">Adiciona as chaves públicas do SSH para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="67173-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67173-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67173-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="67173-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67173-105">DESCRIPTION</span></span>
<span data-ttu-id="67173-106">O cmdlet **Add-AzureRmVMSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar a uma máquina virtual sobre o Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="67173-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="67173-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67173-107">EXAMPLES</span></span>

### <span data-ttu-id="67173-108">Exemplo 1: adicionar uma chave pública a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="67173-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="67173-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="67173-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="67173-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="67173-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="67173-111">O segundo comando adiciona a chave pública ao local em VirtualMachine07 que o parâmetro path especifica.</span><span class="sxs-lookup"><span data-stu-id="67173-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="67173-112">OS</span><span class="sxs-lookup"><span data-stu-id="67173-112">PARAMETERS</span></span>

### <span data-ttu-id="67173-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="67173-113">-KeyData</span></span>
<span data-ttu-id="67173-114">Especifica uma codificação base 64 de uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="67173-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="67173-115">Você pode se conectar a uma máquina virtual usando SSH ou usando a chave que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="67173-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67173-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="67173-116">-Path</span></span>
<span data-ttu-id="67173-117">Especifica o caminho completo de um arquivo, na máquina virtual, em que esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="67173-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="67173-118">Se o arquivo já existir, esse cmdlet acrescentará a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="67173-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="67173-119">-VM</span><span class="sxs-lookup"><span data-stu-id="67173-119">-VM</span></span>
<span data-ttu-id="67173-120">Especifica o objeto da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="67173-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="67173-121">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="67173-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="67173-122">Você pode usar o cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="67173-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67173-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67173-123">CommonParameters</span></span>
<span data-ttu-id="67173-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67173-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67173-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67173-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67173-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67173-126">INPUTS</span></span>

### <span data-ttu-id="67173-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="67173-127">None</span></span>
<span data-ttu-id="67173-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="67173-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67173-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67173-129">OUTPUTS</span></span>

## <span data-ttu-id="67173-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67173-130">NOTES</span></span>

## <span data-ttu-id="67173-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67173-131">RELATED LINKS</span></span>

[<span data-ttu-id="67173-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67173-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="67173-133">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="67173-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
