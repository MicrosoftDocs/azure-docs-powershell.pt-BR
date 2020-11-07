---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786035"
---
# <span data-ttu-id="0ac87-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="0ac87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ac87-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac87-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac87-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ac87-104">SYNTAX</span></span>

### <span data-ttu-id="0ac87-105">Eles</span><span class="sxs-lookup"><span data-stu-id="0ac87-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ac87-106">S2</span><span class="sxs-lookup"><span data-stu-id="0ac87-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ac87-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ac87-107">DESCRIPTION</span></span>
<span data-ttu-id="0ac87-108">O cmdlet **Stop-AzureRmWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac87-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="0ac87-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ac87-109">EXAMPLES</span></span>

### <span data-ttu-id="0ac87-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="0ac87-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0ac87-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="0ac87-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0ac87-112">OS</span><span class="sxs-lookup"><span data-stu-id="0ac87-112">PARAMETERS</span></span>

### <span data-ttu-id="0ac87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac87-113">-DefaultProfile</span></span>
<span data-ttu-id="0ac87-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ac87-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ac87-115">-Name</span></span>
<span data-ttu-id="0ac87-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac87-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ac87-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0ac87-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac87-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-119">-WebApp</span></span>
<span data-ttu-id="0ac87-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac87-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac87-121">CommonParameters</span></span>
<span data-ttu-id="0ac87-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac87-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac87-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac87-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac87-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ac87-124">INPUTS</span></span>

### <span data-ttu-id="0ac87-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="0ac87-125">Site</span></span>
<span data-ttu-id="0ac87-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="0ac87-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0ac87-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ac87-127">OUTPUTS</span></span>

## <span data-ttu-id="0ac87-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ac87-128">NOTES</span></span>

## <span data-ttu-id="0ac87-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ac87-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ac87-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0ac87-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0ac87-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0ac87-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0ac87-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0ac87-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


