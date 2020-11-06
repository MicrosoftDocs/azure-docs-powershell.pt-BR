---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433350"
---
# <span data-ttu-id="79298-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="79298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79298-102">SYNOPSIS</span></span>
<span data-ttu-id="79298-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="79298-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79298-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79298-104">SYNTAX</span></span>

### <span data-ttu-id="79298-105">Eles</span><span class="sxs-lookup"><span data-stu-id="79298-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79298-106">S2</span><span class="sxs-lookup"><span data-stu-id="79298-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79298-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79298-107">DESCRIPTION</span></span>
<span data-ttu-id="79298-108">O cmdlet **Stop-AzureRmWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="79298-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="79298-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79298-109">EXAMPLES</span></span>

### <span data-ttu-id="79298-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="79298-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="79298-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="79298-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="79298-112">OS</span><span class="sxs-lookup"><span data-stu-id="79298-112">PARAMETERS</span></span>

### <span data-ttu-id="79298-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79298-113">-DefaultProfile</span></span>
<span data-ttu-id="79298-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79298-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79298-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="79298-115">-Name</span></span>
<span data-ttu-id="79298-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="79298-116">WebApp Name</span></span>

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

### <span data-ttu-id="79298-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79298-117">-ResourceGroupName</span></span>
<span data-ttu-id="79298-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="79298-118">Resource Group Name</span></span>

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

### <span data-ttu-id="79298-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="79298-119">-WebApp</span></span>
<span data-ttu-id="79298-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="79298-120">WebApp Object</span></span>

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

### <span data-ttu-id="79298-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79298-121">CommonParameters</span></span>
<span data-ttu-id="79298-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79298-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79298-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79298-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79298-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79298-124">INPUTS</span></span>

### <span data-ttu-id="79298-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="79298-125">Site</span></span>
<span data-ttu-id="79298-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="79298-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="79298-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79298-127">OUTPUTS</span></span>

## <span data-ttu-id="79298-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79298-128">NOTES</span></span>

## <span data-ttu-id="79298-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79298-129">RELATED LINKS</span></span>

[<span data-ttu-id="79298-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="79298-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="79298-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="79298-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="79298-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="79298-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


