---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: d54bc01e7a5aa23206037d4eb1d99e5d9e5deb0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432751"
---
# <span data-ttu-id="8a1ed-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="8a1ed-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="8a1ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1ed-103">Regenera a tecla de acesso de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a1ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a1ed-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a1ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a1ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1ed-106">O cmdlet **New-AzureRmRedisCacheKey** regenera a tecla de acesso de um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="8a1ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a1ed-107">EXAMPLES</span></span>

### <span data-ttu-id="8a1ed-108">Exemplo 1: regenerar uma chave primária</span><span class="sxs-lookup"><span data-stu-id="8a1ed-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="8a1ed-109">Esse comando regenera a chave primária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="8a1ed-110">Exemplo 2: regenerar uma chave secundária</span><span class="sxs-lookup"><span data-stu-id="8a1ed-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="8a1ed-111">Esse comando regenera a chave secundária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="8a1ed-112">OS</span><span class="sxs-lookup"><span data-stu-id="8a1ed-112">PARAMETERS</span></span>

### <span data-ttu-id="8a1ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1ed-113">-DefaultProfile</span></span>
<span data-ttu-id="8a1ed-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a1ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a1ed-115">-Force</span></span>
<span data-ttu-id="8a1ed-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1ed-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8a1ed-117">-KeyType</span></span>
<span data-ttu-id="8a1ed-118">Especifica se a chave de acesso primária ou secundária deve ser regerada.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="8a1ed-119">Os valores válidos são: principal, secundário.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a1ed-120">-Name</span></span>
<span data-ttu-id="8a1ed-121">Especifica o nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="8a1ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a1ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a1ed-123">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="8a1ed-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a1ed-124">-Confirm</span></span>
<span data-ttu-id="8a1ed-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1ed-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a1ed-126">-WhatIf</span></span>
<span data-ttu-id="8a1ed-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a1ed-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1ed-129">CommonParameters</span></span>
<span data-ttu-id="8a1ed-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1ed-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a1ed-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1ed-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a1ed-132">INPUTS</span></span>

### <span data-ttu-id="8a1ed-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a1ed-133">System.String</span></span>

## <span data-ttu-id="8a1ed-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a1ed-134">OUTPUTS</span></span>

### <span data-ttu-id="8a1ed-135">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8a1ed-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="8a1ed-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a1ed-136">NOTES</span></span>

## <span data-ttu-id="8a1ed-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a1ed-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a1ed-138">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="8a1ed-138">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


