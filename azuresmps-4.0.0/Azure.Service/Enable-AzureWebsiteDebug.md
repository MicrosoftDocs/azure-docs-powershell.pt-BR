---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946374"
---
# <span data-ttu-id="8f69f-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="8f69f-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="8f69f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f69f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f69f-103">Habilita a depuração do site.</span><span class="sxs-lookup"><span data-stu-id="8f69f-103">Enables the website's debug.</span></span>

## <span data-ttu-id="8f69f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f69f-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f69f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f69f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f69f-106">Habilita o recurso de depuração do site no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8f69f-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="8f69f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f69f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f69f-108">Habilitar a depuração do Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="8f69f-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="8f69f-109">Habilita a depuração no VS 2013.</span><span class="sxs-lookup"><span data-stu-id="8f69f-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="8f69f-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f69f-110">PARAMETERS</span></span>

### <span data-ttu-id="8f69f-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f69f-111">-Name</span></span>
<span data-ttu-id="8f69f-112">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f69f-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="8f69f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f69f-113">-PassThru</span></span>
<span data-ttu-id="8f69f-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8f69f-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f69f-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8f69f-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f69f-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8f69f-116">-Profile</span></span>
<span data-ttu-id="8f69f-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8f69f-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f69f-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8f69f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f69f-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8f69f-119">-Slot</span></span>
<span data-ttu-id="8f69f-120">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f69f-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="8f69f-121">-Versão</span><span class="sxs-lookup"><span data-stu-id="8f69f-121">-Version</span></span>
<span data-ttu-id="8f69f-122">A versão do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8f69f-122">The Visual Studio version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f69f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f69f-123">CommonParameters</span></span>
<span data-ttu-id="8f69f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f69f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f69f-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f69f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f69f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f69f-126">INPUTS</span></span>

## <span data-ttu-id="8f69f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f69f-127">OUTPUTS</span></span>

## <span data-ttu-id="8f69f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f69f-128">NOTES</span></span>

## <span data-ttu-id="8f69f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f69f-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f69f-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="8f69f-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="8f69f-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f69f-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8f69f-132">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f69f-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8f69f-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f69f-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="8f69f-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8f69f-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


