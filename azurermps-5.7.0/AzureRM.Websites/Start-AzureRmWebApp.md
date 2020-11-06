---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 74f0fcfdcbbc71781debef62becb36018ecb51a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426535"
---
# <span data-ttu-id="98d5f-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="98d5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="98d5f-103">Inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="98d5f-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98d5f-104">SYNTAX</span></span>

### <span data-ttu-id="98d5f-105">Eles</span><span class="sxs-lookup"><span data-stu-id="98d5f-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98d5f-106">S2</span><span class="sxs-lookup"><span data-stu-id="98d5f-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d5f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98d5f-107">DESCRIPTION</span></span>
<span data-ttu-id="98d5f-108">O cmdlet **Start-AzureRmWebApp** inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="98d5f-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="98d5f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98d5f-109">EXAMPLES</span></span>

### <span data-ttu-id="98d5f-110">Exemplo 1: iniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="98d5f-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="98d5f-111">Esse comando inicia o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="98d5f-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="98d5f-112">OS</span><span class="sxs-lookup"><span data-stu-id="98d5f-112">PARAMETERS</span></span>

### <span data-ttu-id="98d5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d5f-113">-DefaultProfile</span></span>
<span data-ttu-id="98d5f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98d5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d5f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="98d5f-115">-Name</span></span>
<span data-ttu-id="98d5f-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-116">WebApp Name</span></span>

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

### <span data-ttu-id="98d5f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d5f-117">-ResourceGroupName</span></span>
<span data-ttu-id="98d5f-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="98d5f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="98d5f-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-119">-WebApp</span></span>
<span data-ttu-id="98d5f-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-120">WebApp Object</span></span>

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

### <span data-ttu-id="98d5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d5f-121">CommonParameters</span></span>
<span data-ttu-id="98d5f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d5f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d5f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d5f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98d5f-124">INPUTS</span></span>

### <span data-ttu-id="98d5f-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="98d5f-125">Site</span></span>
<span data-ttu-id="98d5f-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="98d5f-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="98d5f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98d5f-127">OUTPUTS</span></span>

## <span data-ttu-id="98d5f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98d5f-128">NOTES</span></span>

## <span data-ttu-id="98d5f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98d5f-129">RELATED LINKS</span></span>

[<span data-ttu-id="98d5f-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="98d5f-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="98d5f-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="98d5f-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="98d5f-134">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="98d5f-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


