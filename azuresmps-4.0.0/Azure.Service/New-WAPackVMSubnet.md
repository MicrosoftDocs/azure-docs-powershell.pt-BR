---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945886"
---
# <span data-ttu-id="11828-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="11828-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="11828-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11828-102">SYNOPSIS</span></span>
<span data-ttu-id="11828-103">Cria uma sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="11828-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11828-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="11828-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11828-105">DESCRIPTION</span></span>
<span data-ttu-id="11828-106">O cmdlet **New-WAPackVMSubnet** cria uma sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="11828-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11828-107">EXAMPLES</span></span>

### <span data-ttu-id="11828-108">Exemplo 1: criar uma sub-rede de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="11828-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="11828-109">O primeiro comando recupera a rede de máquina virtual à qual queremos adicionar uma nova sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="11828-110">Esta rede de máquina virtual se chama ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="11828-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="11828-111">O segundo comando cria uma sub-rede de máquina virtual usando a rede da máquina virtual de recuperação anterior, um nome ContosoVMSubnet01 e uma sub-rede 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="11828-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="11828-112">OS</span><span class="sxs-lookup"><span data-stu-id="11828-112">PARAMETERS</span></span>

### <span data-ttu-id="11828-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="11828-113">-Name</span></span>
<span data-ttu-id="11828-114">Especifica um nome para a sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-114">Specifies a name for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11828-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="11828-115">-Profile</span></span>
<span data-ttu-id="11828-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="11828-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11828-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="11828-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11828-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="11828-118">-Subnet</span></span>
<span data-ttu-id="11828-119">Especifica uma sub-rede para a sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-119">Specifies a subnet for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11828-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="11828-120">-VNet</span></span>
<span data-ttu-id="11828-121">Especifica uma VNet associada à sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11828-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11828-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11828-122">CommonParameters</span></span>
<span data-ttu-id="11828-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11828-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11828-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11828-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11828-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11828-125">INPUTS</span></span>

## <span data-ttu-id="11828-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11828-126">OUTPUTS</span></span>

## <span data-ttu-id="11828-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11828-127">NOTES</span></span>

## <span data-ttu-id="11828-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11828-128">RELATED LINKS</span></span>

[<span data-ttu-id="11828-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="11828-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="11828-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="11828-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="11828-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="11828-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


