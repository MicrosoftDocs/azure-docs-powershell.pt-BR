---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945691"
---
# <span data-ttu-id="c61db-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="c61db-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="c61db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c61db-102">SYNOPSIS</span></span>
<span data-ttu-id="c61db-103">Desabilita a depuração do site.</span><span class="sxs-lookup"><span data-stu-id="c61db-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="c61db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c61db-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c61db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c61db-105">DESCRIPTION</span></span>
<span data-ttu-id="c61db-106">Desabilita a depuração do site no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c61db-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="c61db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c61db-107">EXAMPLES</span></span>

### <span data-ttu-id="c61db-108">--------------Desabilitar a depuração de site--------------</span><span class="sxs-lookup"><span data-stu-id="c61db-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="c61db-109">Desabilita a depuração de site no site mywebsite</span><span class="sxs-lookup"><span data-stu-id="c61db-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="c61db-110">OS</span><span class="sxs-lookup"><span data-stu-id="c61db-110">PARAMETERS</span></span>

### <span data-ttu-id="c61db-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c61db-111">-Name</span></span>
<span data-ttu-id="c61db-112">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c61db-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="c61db-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c61db-113">-PassThru</span></span>
<span data-ttu-id="c61db-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c61db-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c61db-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c61db-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61db-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c61db-116">-Profile</span></span>
<span data-ttu-id="c61db-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c61db-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c61db-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c61db-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c61db-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="c61db-119">-Slot</span></span>
<span data-ttu-id="c61db-120">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="c61db-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="c61db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61db-121">CommonParameters</span></span>
<span data-ttu-id="c61db-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61db-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61db-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61db-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c61db-124">INPUTS</span></span>

## <span data-ttu-id="c61db-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c61db-125">OUTPUTS</span></span>

## <span data-ttu-id="c61db-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c61db-126">NOTES</span></span>

## <span data-ttu-id="c61db-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c61db-127">RELATED LINKS</span></span>

[<span data-ttu-id="c61db-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="c61db-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="c61db-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c61db-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="c61db-130">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c61db-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="c61db-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c61db-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="c61db-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c61db-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


