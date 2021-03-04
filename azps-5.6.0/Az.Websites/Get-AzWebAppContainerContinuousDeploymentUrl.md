---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889105"
---
# <span data-ttu-id="1ac4e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="1ac4e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="1ac4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac4e-103">Get-AzWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="1ac4e-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="1ac4e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ac4e-104">SYNTAX</span></span>

### <span data-ttu-id="1ac4e-105">S1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ac4e-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ac4e-106">S2</span><span class="sxs-lookup"><span data-stu-id="1ac4e-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac4e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ac4e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac4e-108">Get-AzWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="1ac4e-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="1ac4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ac4e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ac4e-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="1ac4e-111">Este comando retornará a URL de implantação contínua do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="1ac4e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-112">PARAMETERS</span></span>

### <span data-ttu-id="1ac4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac4e-113">-DefaultProfile</span></span>
<span data-ttu-id="1ac4e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac4e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1ac4e-115">-Name</span></span>
<span data-ttu-id="1ac4e-116">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-116">The name of the web app.</span></span>

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

### <span data-ttu-id="1ac4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ac4e-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ac4e-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="1ac4e-119">-SlotName</span></span>
<span data-ttu-id="1ac4e-120">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac4e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1ac4e-121">-WebApp</span></span>
<span data-ttu-id="1ac4e-122">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="1ac4e-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac4e-123">CommonParameters</span></span>
<span data-ttu-id="1ac4e-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac4e-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac4e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac4e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-126">INPUTS</span></span>

### <span data-ttu-id="1ac4e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1ac4e-127">System.String</span></span>

### <span data-ttu-id="1ac4e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1ac4e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1ac4e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-129">OUTPUTS</span></span>

### <span data-ttu-id="1ac4e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1ac4e-130">System.String</span></span>

## <span data-ttu-id="1ac4e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ac4e-131">NOTES</span></span>

## <span data-ttu-id="1ac4e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ac4e-132">RELATED LINKS</span></span>
