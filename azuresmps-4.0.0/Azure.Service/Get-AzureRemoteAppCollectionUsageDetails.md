---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945632"
---
# <span data-ttu-id="fd71a-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="fd71a-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="fd71a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd71a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd71a-103">Recupera os detalhes de uso de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd71a-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="fd71a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd71a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd71a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd71a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd71a-106">O cmdlet **Get-AzureRemoteAppCollectionUsageDetails** recupera detalhes de uso de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd71a-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="fd71a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd71a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd71a-108">Exemplo 1: obter detalhes de uso de uma coleção</span><span class="sxs-lookup"><span data-stu-id="fd71a-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="fd71a-109">Esse comando obtém detalhes de uso do mês de dezembro no ano 2014 para um conjunto do Azure RemoteApp chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="fd71a-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="fd71a-110">OS</span><span class="sxs-lookup"><span data-stu-id="fd71a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd71a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd71a-111">-AsJob</span></span>
<span data-ttu-id="fd71a-112">Indica que o cmdlet é executado em segundo plano como um trabalho do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fd71a-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="fd71a-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="fd71a-113">-CollectionName</span></span>
<span data-ttu-id="fd71a-114">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd71a-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="fd71a-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fd71a-115">-Profile</span></span>
<span data-ttu-id="fd71a-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fd71a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd71a-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fd71a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd71a-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="fd71a-118">-UsageMonth</span></span>
<span data-ttu-id="fd71a-119">Especifica um número de dois dígitos para o mês para o qual obter detalhes de uso.</span><span class="sxs-lookup"><span data-stu-id="fd71a-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="fd71a-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="fd71a-120">-UsageYear</span></span>
<span data-ttu-id="fd71a-121">Especifica o ano de quatro dígitos para o qual obter detalhes de uso.</span><span class="sxs-lookup"><span data-stu-id="fd71a-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="fd71a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd71a-122">CommonParameters</span></span>
<span data-ttu-id="fd71a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd71a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd71a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd71a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd71a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd71a-125">INPUTS</span></span>

## <span data-ttu-id="fd71a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd71a-126">OUTPUTS</span></span>

## <span data-ttu-id="fd71a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd71a-127">NOTES</span></span>

## <span data-ttu-id="fd71a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd71a-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd71a-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fd71a-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="fd71a-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="fd71a-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


