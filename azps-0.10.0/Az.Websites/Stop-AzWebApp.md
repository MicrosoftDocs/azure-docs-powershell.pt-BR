---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776044"
---
# <span data-ttu-id="d64a4-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="d64a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d64a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d64a4-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d64a4-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="d64a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d64a4-104">SYNTAX</span></span>

### <span data-ttu-id="d64a4-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d64a4-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d64a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="d64a4-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d64a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d64a4-107">DESCRIPTION</span></span>
<span data-ttu-id="d64a4-108">O cmdlet **Stop-AzWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d64a4-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="d64a4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d64a4-109">EXAMPLES</span></span>

### <span data-ttu-id="d64a4-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d64a4-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d64a4-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d64a4-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d64a4-112">OS</span><span class="sxs-lookup"><span data-stu-id="d64a4-112">PARAMETERS</span></span>

### <span data-ttu-id="d64a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64a4-113">-DefaultProfile</span></span>
<span data-ttu-id="d64a4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d64a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d64a4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d64a4-115">-Name</span></span>
<span data-ttu-id="d64a4-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-116">WebApp Name</span></span>

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

### <span data-ttu-id="d64a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d64a4-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d64a4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d64a4-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-119">-WebApp</span></span>
<span data-ttu-id="d64a4-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-120">WebApp Object</span></span>

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

### <span data-ttu-id="d64a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64a4-121">CommonParameters</span></span>
<span data-ttu-id="d64a4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64a4-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64a4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64a4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d64a4-124">INPUTS</span></span>

### <span data-ttu-id="d64a4-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="d64a4-125">Site</span></span>
<span data-ttu-id="d64a4-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="d64a4-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d64a4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d64a4-127">OUTPUTS</span></span>

## <span data-ttu-id="d64a4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d64a4-128">NOTES</span></span>

## <span data-ttu-id="d64a4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d64a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="d64a4-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d64a4-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d64a4-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d64a4-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d64a4-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d64a4-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


