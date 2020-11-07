---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
ms.openlocfilehash: c8109a1fa13bff2a2a527bb7e1f9cb232d0e61c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786190"
---
# <span data-ttu-id="10b26-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="10b26-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="10b26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10b26-102">SYNOPSIS</span></span>
<span data-ttu-id="10b26-103">Adiciona as chaves públicas do SSH para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="10b26-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10b26-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10b26-105">DESCRIPTION</span></span>
<span data-ttu-id="10b26-106">O cmdlet **Add-AzureRmVMSshPublicKey** adiciona as chaves públicas que você pode usar para se conectar a uma máquina virtual sobre o Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="10b26-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="10b26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10b26-107">EXAMPLES</span></span>

### <span data-ttu-id="10b26-108">Exemplo 1: adicionar uma chave pública a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="10b26-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="10b26-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="10b26-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="10b26-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="10b26-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="10b26-111">O segundo comando adiciona a chave pública ao local em VirtualMachine07 que o parâmetro path especifica.</span><span class="sxs-lookup"><span data-stu-id="10b26-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="10b26-112">OS</span><span class="sxs-lookup"><span data-stu-id="10b26-112">PARAMETERS</span></span>

### <span data-ttu-id="10b26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b26-113">-DefaultProfile</span></span>
<span data-ttu-id="10b26-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10b26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b26-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="10b26-115">-KeyData</span></span>
<span data-ttu-id="10b26-116">Especifica uma codificação base 64 de uma chave pública.</span><span class="sxs-lookup"><span data-stu-id="10b26-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="10b26-117">Você pode se conectar a uma máquina virtual usando SSH ou usando a chave que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="10b26-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="10b26-118">-Caminho</span><span class="sxs-lookup"><span data-stu-id="10b26-118">-Path</span></span>
<span data-ttu-id="10b26-119">Especifica o caminho completo de um arquivo, na máquina virtual, em que esse cmdlet armazena a chave pública SSH.</span><span class="sxs-lookup"><span data-stu-id="10b26-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="10b26-120">Se o arquivo já existir, esse cmdlet acrescentará a chave ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="10b26-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="10b26-121">-VM</span><span class="sxs-lookup"><span data-stu-id="10b26-121">-VM</span></span>
<span data-ttu-id="10b26-122">Especifica o objeto da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="10b26-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="10b26-123">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="10b26-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="10b26-124">Você pode usar o cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="10b26-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="10b26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b26-125">CommonParameters</span></span>
<span data-ttu-id="10b26-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b26-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b26-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b26-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10b26-128">INPUTS</span></span>

### <span data-ttu-id="10b26-129">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="10b26-129">PSVirtualMachine</span></span>
<span data-ttu-id="10b26-130">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="10b26-130">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="10b26-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10b26-131">OUTPUTS</span></span>

### <span data-ttu-id="10b26-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="10b26-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="10b26-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10b26-133">NOTES</span></span>

## <span data-ttu-id="10b26-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10b26-134">RELATED LINKS</span></span>

[<span data-ttu-id="10b26-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10b26-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="10b26-136">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="10b26-136">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
