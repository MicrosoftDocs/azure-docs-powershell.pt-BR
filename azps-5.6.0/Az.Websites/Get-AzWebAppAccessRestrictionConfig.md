---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889365"
---
# <span data-ttu-id="03b81-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="03b81-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="03b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b81-102">SYNOPSIS</span></span>
<span data-ttu-id="03b81-103">Obtém a configuração de Restiction do Access para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="03b81-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="03b81-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03b81-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b81-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03b81-105">DESCRIPTION</span></span>
<span data-ttu-id="03b81-106">O cmdlet **Get-AzWebAppAccessRestrictionConfig obtém** a config Restrição de Acesso sobre um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="03b81-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="03b81-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03b81-107">EXAMPLES</span></span>

### <span data-ttu-id="03b81-108">Exemplo 1: Obter uma Configuração de Restrição de Acesso a Aplicativo Web de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="03b81-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="03b81-109">Este comando obtém a configuração de restrição de acesso de um Aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="03b81-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="03b81-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03b81-110">PARAMETERS</span></span>

### <span data-ttu-id="03b81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b81-111">-DefaultProfile</span></span>
<span data-ttu-id="03b81-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="03b81-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03b81-113">-Name</span><span class="sxs-lookup"><span data-stu-id="03b81-113">-Name</span></span>
<span data-ttu-id="03b81-114">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="03b81-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b81-115">-ResourceGroupName</span></span>
<span data-ttu-id="03b81-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="03b81-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="03b81-117">-SlotName</span></span>
<span data-ttu-id="03b81-118">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="03b81-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b81-119">CommonParameters</span></span>
<span data-ttu-id="03b81-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b81-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03b81-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b81-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03b81-122">INPUTS</span></span>

### <span data-ttu-id="03b81-123">System.String</span><span class="sxs-lookup"><span data-stu-id="03b81-123">System.String</span></span>

## <span data-ttu-id="03b81-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03b81-124">OUTPUTS</span></span>

### <span data-ttu-id="03b81-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="03b81-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="03b81-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="03b81-126">NOTES</span></span>

## <span data-ttu-id="03b81-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03b81-127">RELATED LINKS</span></span>

[<span data-ttu-id="03b81-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="03b81-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="03b81-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="03b81-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="03b81-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="03b81-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
