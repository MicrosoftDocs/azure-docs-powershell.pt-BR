---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257260"
---
# <span data-ttu-id="49771-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="49771-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="49771-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49771-102">SYNOPSIS</span></span>
<span data-ttu-id="49771-103">Obtém a configuração do restiction de acesso para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="49771-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="49771-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49771-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49771-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49771-105">DESCRIPTION</span></span>
<span data-ttu-id="49771-106">O cmdlet **Get-AzWebAppAccessRestrictionConfig** Obtém a configuração de restrição de acesso sobre um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="49771-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="49771-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49771-107">EXAMPLES</span></span>

### <span data-ttu-id="49771-108">Exemplo 1: obter uma configuração de restrição de acesso do aplicativo Web a partir de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="49771-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="49771-109">Esse comando obtém a configuração de restrição de acesso de um aplicativo Web chamado ContosoSite que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="49771-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="49771-110">OS</span><span class="sxs-lookup"><span data-stu-id="49771-110">PARAMETERS</span></span>

### <span data-ttu-id="49771-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49771-111">-DefaultProfile</span></span>
<span data-ttu-id="49771-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49771-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49771-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="49771-113">-Name</span></span>
<span data-ttu-id="49771-114">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="49771-114">WebApp Name</span></span>

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

### <span data-ttu-id="49771-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49771-115">-ResourceGroupName</span></span>
<span data-ttu-id="49771-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="49771-116">Resource Group Name</span></span>

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

### <span data-ttu-id="49771-117">-Slotname</span><span class="sxs-lookup"><span data-stu-id="49771-117">-SlotName</span></span>
<span data-ttu-id="49771-118">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="49771-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="49771-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49771-119">CommonParameters</span></span>
<span data-ttu-id="49771-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49771-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49771-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49771-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49771-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49771-122">INPUTS</span></span>

### <span data-ttu-id="49771-123">System. String</span><span class="sxs-lookup"><span data-stu-id="49771-123">System.String</span></span>

## <span data-ttu-id="49771-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49771-124">OUTPUTS</span></span>

### <span data-ttu-id="49771-125">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="49771-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="49771-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49771-126">NOTES</span></span>

## <span data-ttu-id="49771-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49771-127">RELATED LINKS</span></span>

[<span data-ttu-id="49771-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="49771-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="49771-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="49771-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="49771-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="49771-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
