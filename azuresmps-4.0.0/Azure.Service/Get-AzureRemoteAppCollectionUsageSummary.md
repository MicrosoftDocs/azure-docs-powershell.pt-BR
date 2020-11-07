---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946330"
---
# <span data-ttu-id="182a0-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="182a0-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="182a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="182a0-102">SYNOPSIS</span></span>
<span data-ttu-id="182a0-103">Recupera um resumo de uso para uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="182a0-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="182a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="182a0-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="182a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="182a0-105">DESCRIPTION</span></span>
<span data-ttu-id="182a0-106">O cmdlet **Get-AzureRemoteAppCollectionUsageSummary** recupera um resumo de uso para uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="182a0-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="182a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="182a0-107">EXAMPLES</span></span>

### <span data-ttu-id="182a0-108">Exemplo 1: obter um resumo de uso</span><span class="sxs-lookup"><span data-stu-id="182a0-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="182a0-109">Esse comando obtém um resumo de uso do mês de dezembro no ano 2014, para uma coleção chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="182a0-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="182a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="182a0-110">PARAMETERS</span></span>

### <span data-ttu-id="182a0-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="182a0-111">-CollectionName</span></span>
<span data-ttu-id="182a0-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="182a0-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182a0-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="182a0-113">-Profile</span></span>
<span data-ttu-id="182a0-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="182a0-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="182a0-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="182a0-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="182a0-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="182a0-116">-UsageMonth</span></span>
<span data-ttu-id="182a0-117">Especifica um número de dois dígitos para o mês para o qual obter um resumo de uso.</span><span class="sxs-lookup"><span data-stu-id="182a0-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="182a0-118">Se esse parâmetro não for especificado, esse cmdlet fornecerá o uso para o mês atual.</span><span class="sxs-lookup"><span data-stu-id="182a0-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182a0-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="182a0-119">-UsageYear</span></span>
<span data-ttu-id="182a0-120">Especifica o ano de quatro dígitos para o qual obter um resumo de uso.</span><span class="sxs-lookup"><span data-stu-id="182a0-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="182a0-121">Se esse parâmetro não for especificado, esse cmdlet fornecerá um resumo de uso para o ano atual será usado.</span><span class="sxs-lookup"><span data-stu-id="182a0-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182a0-122">CommonParameters</span></span>
<span data-ttu-id="182a0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="182a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182a0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182a0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="182a0-125">INPUTS</span></span>

## <span data-ttu-id="182a0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="182a0-126">OUTPUTS</span></span>

## <span data-ttu-id="182a0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="182a0-127">NOTES</span></span>

## <span data-ttu-id="182a0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="182a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="182a0-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="182a0-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="182a0-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="182a0-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


