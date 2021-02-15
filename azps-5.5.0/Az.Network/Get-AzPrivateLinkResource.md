---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112897"
---
# <span data-ttu-id="0ffdc-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0ffdc-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="0ffdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ffdc-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffdc-103">Obtém um recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-103">Gets a private link resource.</span></span>

## <span data-ttu-id="0ffdc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ffdc-104">SYNTAX</span></span>

### <span data-ttu-id="0ffdc-105">ByPrivateLinkResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0ffdc-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ffdc-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="0ffdc-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="0ffdc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ffdc-107">DESCRIPTION</span></span>
<span data-ttu-id="0ffdc-108">O cmdlet **Get-AzPrivateLinkResource** recupera todos os recursos de link que pertencem a PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="0ffdc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ffdc-109">EXAMPLES</span></span>

### <span data-ttu-id="0ffdc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ffdc-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="0ffdc-111">Este exemplo lista todos os recursos de link particular ao sql server chamado mySql.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="0ffdc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ffdc-112">PARAMETERS</span></span>

### <span data-ttu-id="0ffdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffdc-113">-DefaultProfile</span></span>
<span data-ttu-id="0ffdc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ffdc-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0ffdc-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0ffdc-116">A ID do gerenciador de recursos do Azure do recurso de vinculação privada.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffdc-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0ffdc-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0ffdc-118">O tipo de recurso de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ffdc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffdc-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0ffdc-121">-ServiceName</span></span>
<span data-ttu-id="0ffdc-122">O nome do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffdc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffdc-123">CommonParameters</span></span>
<span data-ttu-id="0ffdc-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffdc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffdc-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ffdc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffdc-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ffdc-126">INPUTS</span></span>

### <span data-ttu-id="0ffdc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0ffdc-127">System.String</span></span>

## <span data-ttu-id="0ffdc-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ffdc-128">OUTPUTS</span></span>

### <span data-ttu-id="0ffdc-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ffdc-129">System.Boolean</span></span>

## <span data-ttu-id="0ffdc-130">Notas</span><span class="sxs-lookup"><span data-stu-id="0ffdc-130">NOTES</span></span>

## <span data-ttu-id="0ffdc-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ffdc-131">RELATED LINKS</span></span>
