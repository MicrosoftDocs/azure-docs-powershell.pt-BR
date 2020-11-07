---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946545"
---
# <span data-ttu-id="01485-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="01485-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="01485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01485-102">SYNOPSIS</span></span>
<span data-ttu-id="01485-103">Obtém a extensão chefe aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="01485-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="01485-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01485-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="01485-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01485-105">DESCRIPTION</span></span>
<span data-ttu-id="01485-106">O cmdlet **Get-AzureVMChefExtension** Obtém a extensão chefe aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="01485-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="01485-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01485-107">EXAMPLES</span></span>

### <span data-ttu-id="01485-108">Exemplo 1: obter a extensão chefe aplicada na máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="01485-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="01485-109">Este comando obtém a extensão chefe aplicada na máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="01485-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="01485-110">OS</span><span class="sxs-lookup"><span data-stu-id="01485-110">PARAMETERS</span></span>

### <span data-ttu-id="01485-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="01485-111">-InformationAction</span></span>
<span data-ttu-id="01485-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="01485-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="01485-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="01485-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01485-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="01485-114">Continue</span></span>
- <span data-ttu-id="01485-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="01485-115">Ignore</span></span>
- <span data-ttu-id="01485-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="01485-116">Inquire</span></span>
- <span data-ttu-id="01485-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="01485-117">SilentlyContinue</span></span>
- <span data-ttu-id="01485-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="01485-118">Stop</span></span>
- <span data-ttu-id="01485-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="01485-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01485-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="01485-120">-InformationVariable</span></span>
<span data-ttu-id="01485-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="01485-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01485-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="01485-122">-Profile</span></span>
<span data-ttu-id="01485-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="01485-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01485-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="01485-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01485-125">-VM</span><span class="sxs-lookup"><span data-stu-id="01485-125">-VM</span></span>
<span data-ttu-id="01485-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="01485-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01485-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01485-127">CommonParameters</span></span>
<span data-ttu-id="01485-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01485-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01485-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01485-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01485-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01485-130">INPUTS</span></span>

## <span data-ttu-id="01485-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01485-131">OUTPUTS</span></span>

## <span data-ttu-id="01485-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01485-132">NOTES</span></span>

## <span data-ttu-id="01485-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01485-133">RELATED LINKS</span></span>

[<span data-ttu-id="01485-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="01485-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="01485-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="01485-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


