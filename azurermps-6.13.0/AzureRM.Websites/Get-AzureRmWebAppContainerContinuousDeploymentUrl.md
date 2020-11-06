---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429986"
---
# <span data-ttu-id="aea4b-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="aea4b-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="aea4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aea4b-102">SYNOPSIS</span></span>
<span data-ttu-id="aea4b-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="aea4b-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aea4b-104">SYNTAX</span></span>

### <span data-ttu-id="aea4b-105">Eles</span><span class="sxs-lookup"><span data-stu-id="aea4b-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea4b-106">S2</span><span class="sxs-lookup"><span data-stu-id="aea4b-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea4b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aea4b-107">DESCRIPTION</span></span>
<span data-ttu-id="aea4b-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="aea4b-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="aea4b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aea4b-109">EXAMPLES</span></span>

### <span data-ttu-id="aea4b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aea4b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="aea4b-111">Esse comando retornará a URL de implantação contínua do contêiner.</span><span class="sxs-lookup"><span data-stu-id="aea4b-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="aea4b-112">OS</span><span class="sxs-lookup"><span data-stu-id="aea4b-112">PARAMETERS</span></span>

### <span data-ttu-id="aea4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea4b-113">-DefaultProfile</span></span>
<span data-ttu-id="aea4b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aea4b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea4b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aea4b-115">-Name</span></span>
<span data-ttu-id="aea4b-116">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="aea4b-116">The name of the web app.</span></span>

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

### <span data-ttu-id="aea4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="aea4b-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aea4b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="aea4b-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="aea4b-119">-SlotName</span></span>
<span data-ttu-id="aea4b-120">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="aea4b-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="aea4b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="aea4b-121">-WebApp</span></span>
<span data-ttu-id="aea4b-122">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="aea4b-122">The web app object</span></span>

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

### <span data-ttu-id="aea4b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea4b-123">CommonParameters</span></span>
<span data-ttu-id="aea4b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea4b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea4b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea4b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea4b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aea4b-126">INPUTS</span></span>

### <span data-ttu-id="aea4b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="aea4b-127">System.String</span></span>
### <span data-ttu-id="aea4b-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="aea4b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="aea4b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aea4b-129">OUTPUTS</span></span>

### <span data-ttu-id="aea4b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aea4b-130">System.String</span></span>
## <span data-ttu-id="aea4b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aea4b-131">NOTES</span></span>

## <span data-ttu-id="aea4b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aea4b-132">RELATED LINKS</span></span>
