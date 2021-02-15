---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111460"
---
# <span data-ttu-id="641af-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="641af-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="641af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="641af-102">SYNOPSIS</span></span>
<span data-ttu-id="641af-103">Obtém as teclas de acesso de um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="641af-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="641af-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="641af-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="641af-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="641af-105">DESCRIPTION</span></span>
<span data-ttu-id="641af-106">O cmdlet **Get-AzRedisCacheKey** obtém as teclas de acesso de um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="641af-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="641af-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="641af-107">EXAMPLES</span></span>

### <span data-ttu-id="641af-108">Exemplo 1: Obter as teclas de acesso de um Cache de Redis</span><span class="sxs-lookup"><span data-stu-id="641af-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="641af-109">Esse comando obtém as teclas de acesso chamadas MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="641af-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="641af-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="641af-110">PARAMETERS</span></span>

### <span data-ttu-id="641af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641af-111">-DefaultProfile</span></span>
<span data-ttu-id="641af-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="641af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="641af-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="641af-113">-Name</span></span>
<span data-ttu-id="641af-114">Especifica o nome de um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="641af-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641af-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641af-115">-ResourceGroupName</span></span>
<span data-ttu-id="641af-116">Especifica o nome do grupo de recursos que contém o Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="641af-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641af-117">CommonParameters</span></span>
<span data-ttu-id="641af-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641af-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="641af-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641af-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="641af-120">INPUTS</span></span>

### <span data-ttu-id="641af-121">System.String</span><span class="sxs-lookup"><span data-stu-id="641af-121">System.String</span></span>

## <span data-ttu-id="641af-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="641af-122">OUTPUTS</span></span>

### <span data-ttu-id="641af-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="641af-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="641af-124">Notas</span><span class="sxs-lookup"><span data-stu-id="641af-124">NOTES</span></span>

## <span data-ttu-id="641af-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="641af-125">RELATED LINKS</span></span>

[<span data-ttu-id="641af-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="641af-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


