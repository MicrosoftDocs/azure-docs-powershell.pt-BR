---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: eb75a4fa0ebeb121cd39e591b8cb8d46909deb42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426867"
---
# <span data-ttu-id="e50c9-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="e50c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e50c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e50c9-103">Reinicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e50c9-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e50c9-104">SYNTAX</span></span>

### <span data-ttu-id="e50c9-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e50c9-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e50c9-106">S2</span><span class="sxs-lookup"><span data-stu-id="e50c9-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e50c9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e50c9-107">DESCRIPTION</span></span>
<span data-ttu-id="e50c9-108">O cmdlet **Restart-AzureRmWebApp** interrompe e, em seguida, inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e50c9-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="e50c9-109">Se o aplicativo Web estiver em um estado parado, use o cmdlet Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="e50c9-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="e50c9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e50c9-110">EXAMPLES</span></span>

### <span data-ttu-id="e50c9-111">Exemplo 1: reiniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e50c9-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e50c9-112">Esse comando interrompe o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus e, em seguida, o reinicia.</span><span class="sxs-lookup"><span data-stu-id="e50c9-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="e50c9-113">OS</span><span class="sxs-lookup"><span data-stu-id="e50c9-113">PARAMETERS</span></span>

### <span data-ttu-id="e50c9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e50c9-114">-Name</span></span>
<span data-ttu-id="e50c9-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50c9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50c9-116">-ResourceGroupName</span></span>
<span data-ttu-id="e50c9-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e50c9-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50c9-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-118">-WebApp</span></span>
<span data-ttu-id="e50c9-119">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e50c9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50c9-120">-DefaultProfile</span></span>
<span data-ttu-id="e50c9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e50c9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50c9-122">CommonParameters</span></span>
<span data-ttu-id="e50c9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50c9-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50c9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50c9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e50c9-125">INPUTS</span></span>

### <span data-ttu-id="e50c9-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="e50c9-126">Site</span></span>
<span data-ttu-id="e50c9-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e50c9-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e50c9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e50c9-128">OUTPUTS</span></span>

## <span data-ttu-id="e50c9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e50c9-129">NOTES</span></span>

## <span data-ttu-id="e50c9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e50c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="e50c9-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="e50c9-132">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="e50c9-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="e50c9-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="e50c9-135">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e50c9-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

