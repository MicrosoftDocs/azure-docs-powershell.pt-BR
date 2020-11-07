---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945770"
---
# <span data-ttu-id="ce768-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="ce768-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce768-102">SYNOPSIS</span></span>
<span data-ttu-id="ce768-103">Inicia o site especificado.</span><span class="sxs-lookup"><span data-stu-id="ce768-103">Starts the specified website.</span></span>

## <span data-ttu-id="ce768-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce768-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce768-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce768-105">DESCRIPTION</span></span>
<span data-ttu-id="ce768-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce768-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ce768-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ce768-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ce768-108">O cmdlet **Start-AzureWebsite** inicia um site especificado em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="ce768-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="ce768-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce768-109">EXAMPLES</span></span>

## <span data-ttu-id="ce768-110">OS</span><span class="sxs-lookup"><span data-stu-id="ce768-110">PARAMETERS</span></span>

### <span data-ttu-id="ce768-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce768-111">-Name</span></span>
<span data-ttu-id="ce768-112">Especifica o nome do site para começar.</span><span class="sxs-lookup"><span data-stu-id="ce768-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="ce768-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce768-113">-PassThru</span></span>
<span data-ttu-id="ce768-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ce768-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce768-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ce768-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce768-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ce768-116">-Profile</span></span>
<span data-ttu-id="ce768-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ce768-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce768-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ce768-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce768-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ce768-119">-Slot</span></span>
<span data-ttu-id="ce768-120">Especifica o nome do slot do site.</span><span class="sxs-lookup"><span data-stu-id="ce768-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="ce768-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce768-121">CommonParameters</span></span>
<span data-ttu-id="ce768-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce768-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce768-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce768-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce768-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce768-124">INPUTS</span></span>

## <span data-ttu-id="ce768-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce768-125">OUTPUTS</span></span>

## <span data-ttu-id="ce768-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce768-126">NOTES</span></span>

## <span data-ttu-id="ce768-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce768-127">RELATED LINKS</span></span>

[<span data-ttu-id="ce768-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ce768-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="ce768-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="ce768-131">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="ce768-132">Parar-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce768-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


