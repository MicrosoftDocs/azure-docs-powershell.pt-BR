---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112333"
---
# <span data-ttu-id="1e0ab-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1e0ab-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="1e0ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0ab-103">Obtém a configuração de Restiction do Access para um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="1e0ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e0ab-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e0ab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e0ab-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0ab-106">O cmdlet **Get-AzWebAppAccessRestrictionConfig obtém** a configuração de Restrição do Access sobre um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="1e0ab-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e0ab-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0ab-108">Exemplo 1: Obter uma Configuração de Restrição de Acesso do Web App de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1e0ab-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1e0ab-109">Esse comando obtém a configuração de restrição de acesso de um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1e0ab-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e0ab-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0ab-111">-DefaultProfile</span></span>
<span data-ttu-id="1e0ab-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e0ab-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e0ab-113">-Name</span></span>
<span data-ttu-id="1e0ab-114">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="1e0ab-114">WebApp Name</span></span>

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

### <span data-ttu-id="1e0ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="1e0ab-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1e0ab-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1e0ab-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="1e0ab-117">-SlotName</span></span>
<span data-ttu-id="1e0ab-118">Nome do Slot de Implantação.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="1e0ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0ab-119">CommonParameters</span></span>
<span data-ttu-id="1e0ab-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0ab-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e0ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0ab-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e0ab-122">INPUTS</span></span>

### <span data-ttu-id="1e0ab-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1e0ab-123">System.String</span></span>

## <span data-ttu-id="1e0ab-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e0ab-124">OUTPUTS</span></span>

### <span data-ttu-id="1e0ab-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1e0ab-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="1e0ab-126">Notas</span><span class="sxs-lookup"><span data-stu-id="1e0ab-126">NOTES</span></span>

## <span data-ttu-id="1e0ab-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e0ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="1e0ab-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1e0ab-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="1e0ab-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1e0ab-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="1e0ab-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1e0ab-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
