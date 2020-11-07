---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776058"
---
# <span data-ttu-id="94233-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-101">Start-AzWebApp</span></span>

## <span data-ttu-id="94233-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94233-102">SYNOPSIS</span></span>
<span data-ttu-id="94233-103">Inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="94233-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="94233-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94233-104">SYNTAX</span></span>

### <span data-ttu-id="94233-105">Eles</span><span class="sxs-lookup"><span data-stu-id="94233-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94233-106">S2</span><span class="sxs-lookup"><span data-stu-id="94233-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94233-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94233-107">DESCRIPTION</span></span>
<span data-ttu-id="94233-108">O cmdlet **Start-AzWebApp** inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="94233-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="94233-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94233-109">EXAMPLES</span></span>

### <span data-ttu-id="94233-110">Exemplo 1: iniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="94233-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="94233-111">Esse comando inicia o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="94233-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="94233-112">OS</span><span class="sxs-lookup"><span data-stu-id="94233-112">PARAMETERS</span></span>

### <span data-ttu-id="94233-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94233-113">-DefaultProfile</span></span>
<span data-ttu-id="94233-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94233-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94233-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="94233-115">-Name</span></span>
<span data-ttu-id="94233-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="94233-116">WebApp Name</span></span>

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

### <span data-ttu-id="94233-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94233-117">-ResourceGroupName</span></span>
<span data-ttu-id="94233-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="94233-118">Resource Group Name</span></span>

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

### <span data-ttu-id="94233-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="94233-119">-WebApp</span></span>
<span data-ttu-id="94233-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="94233-120">WebApp Object</span></span>

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

### <span data-ttu-id="94233-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94233-121">CommonParameters</span></span>
<span data-ttu-id="94233-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94233-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94233-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94233-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94233-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94233-124">INPUTS</span></span>

### <span data-ttu-id="94233-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="94233-125">Site</span></span>
<span data-ttu-id="94233-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="94233-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="94233-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94233-127">OUTPUTS</span></span>

## <span data-ttu-id="94233-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94233-128">NOTES</span></span>

## <span data-ttu-id="94233-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94233-129">RELATED LINKS</span></span>

[<span data-ttu-id="94233-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="94233-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="94233-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="94233-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="94233-134">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="94233-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


