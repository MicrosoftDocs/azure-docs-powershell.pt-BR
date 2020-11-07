---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945785"
---
# <span data-ttu-id="e35b6-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="e35b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e35b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e35b6-103">Abre um navegador em um site especificado.</span><span class="sxs-lookup"><span data-stu-id="e35b6-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="e35b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e35b6-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e35b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e35b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e35b6-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e35b6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e35b6-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e35b6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e35b6-108">O cmdlet **show-AzureWebsite** abre um navegador em um site especificado.</span><span class="sxs-lookup"><span data-stu-id="e35b6-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="e35b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e35b6-109">EXAMPLES</span></span>

## <span data-ttu-id="e35b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="e35b6-110">PARAMETERS</span></span>

### <span data-ttu-id="e35b6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e35b6-111">-Name</span></span>
<span data-ttu-id="e35b6-112">Especifica o nome do site a ser aberto no navegador.</span><span class="sxs-lookup"><span data-stu-id="e35b6-112">Specifies the name of the site to open in the browser.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b6-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e35b6-113">-Profile</span></span>
<span data-ttu-id="e35b6-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e35b6-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e35b6-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e35b6-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e35b6-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="e35b6-116">-Slot</span></span>
<span data-ttu-id="e35b6-117">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="e35b6-117">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35b6-118">CommonParameters</span></span>
<span data-ttu-id="e35b6-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35b6-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35b6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35b6-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e35b6-121">INPUTS</span></span>

## <span data-ttu-id="e35b6-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e35b6-122">OUTPUTS</span></span>

## <span data-ttu-id="e35b6-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e35b6-123">NOTES</span></span>

## <span data-ttu-id="e35b6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e35b6-124">RELATED LINKS</span></span>

[<span data-ttu-id="e35b6-125">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="e35b6-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="e35b6-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e35b6-127">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e35b6-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e35b6-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="e35b6-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e35b6-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


