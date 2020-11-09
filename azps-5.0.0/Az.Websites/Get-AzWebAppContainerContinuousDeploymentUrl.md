---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282100"
---
# <span data-ttu-id="17944-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="17944-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="17944-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17944-102">SYNOPSIS</span></span>
<span data-ttu-id="17944-103">Get-AzWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="17944-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="17944-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17944-104">SYNTAX</span></span>

### <span data-ttu-id="17944-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="17944-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17944-106">S2</span><span class="sxs-lookup"><span data-stu-id="17944-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17944-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17944-107">DESCRIPTION</span></span>
<span data-ttu-id="17944-108">Get-AzWebAppContainerContinuousDeploymentUrl retornará a URL de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="17944-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="17944-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17944-109">EXAMPLES</span></span>

### <span data-ttu-id="17944-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17944-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="17944-111">Esse comando retornará a URL de implantação contínua do contêiner.</span><span class="sxs-lookup"><span data-stu-id="17944-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="17944-112">OS</span><span class="sxs-lookup"><span data-stu-id="17944-112">PARAMETERS</span></span>

### <span data-ttu-id="17944-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17944-113">-DefaultProfile</span></span>
<span data-ttu-id="17944-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17944-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17944-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="17944-115">-Name</span></span>
<span data-ttu-id="17944-116">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="17944-116">The name of the web app.</span></span>

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

### <span data-ttu-id="17944-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17944-117">-ResourceGroupName</span></span>
<span data-ttu-id="17944-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17944-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="17944-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="17944-119">-SlotName</span></span>
<span data-ttu-id="17944-120">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="17944-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="17944-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="17944-121">-WebApp</span></span>
<span data-ttu-id="17944-122">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="17944-122">The web app object</span></span>

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

### <span data-ttu-id="17944-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17944-123">CommonParameters</span></span>
<span data-ttu-id="17944-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17944-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17944-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17944-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17944-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17944-126">INPUTS</span></span>

### <span data-ttu-id="17944-127">System. String</span><span class="sxs-lookup"><span data-stu-id="17944-127">System.String</span></span>

### <span data-ttu-id="17944-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="17944-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17944-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17944-129">OUTPUTS</span></span>

### <span data-ttu-id="17944-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17944-130">System.String</span></span>

## <span data-ttu-id="17944-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17944-131">NOTES</span></span>

## <span data-ttu-id="17944-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17944-132">RELATED LINKS</span></span>
