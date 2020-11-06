---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426632"
---
# <span data-ttu-id="252cc-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="252cc-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="252cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="252cc-102">SYNOPSIS</span></span>
<span data-ttu-id="252cc-103">Regenera a tecla de acesso de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="252cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="252cc-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="252cc-105">DESCRIPTION</span></span>
<span data-ttu-id="252cc-106">O cmdlet **New-AzureRmRedisCacheKey** regenera a tecla de acesso de um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="252cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="252cc-107">EXAMPLES</span></span>

### <span data-ttu-id="252cc-108">Exemplo 1: regenerar uma chave primária</span><span class="sxs-lookup"><span data-stu-id="252cc-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="252cc-109">Esse comando regenera a chave primária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="252cc-110">Exemplo 2: regenerar uma chave secundária</span><span class="sxs-lookup"><span data-stu-id="252cc-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="252cc-111">Esse comando regenera a chave secundária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="252cc-112">OS</span><span class="sxs-lookup"><span data-stu-id="252cc-112">PARAMETERS</span></span>

### <span data-ttu-id="252cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252cc-113">-DefaultProfile</span></span>
<span data-ttu-id="252cc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="252cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="252cc-115">-Force</span></span>
<span data-ttu-id="252cc-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="252cc-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="252cc-117">-KeyType</span></span>
<span data-ttu-id="252cc-118">Especifica se a chave de acesso primária ou secundária deve ser regerada.</span><span class="sxs-lookup"><span data-stu-id="252cc-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="252cc-119">Os valores válidos são: principal, secundário.</span><span class="sxs-lookup"><span data-stu-id="252cc-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="252cc-120">-Name</span></span>
<span data-ttu-id="252cc-121">Especifica o nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-121">Specifies the name of the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="252cc-123">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="252cc-124">-Confirm</span></span>
<span data-ttu-id="252cc-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252cc-126">-WhatIf</span></span>
<span data-ttu-id="252cc-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="252cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252cc-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="252cc-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252cc-129">CommonParameters</span></span>
<span data-ttu-id="252cc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252cc-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="252cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252cc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="252cc-132">INPUTS</span></span>

### <span data-ttu-id="252cc-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="252cc-133">None</span></span>
<span data-ttu-id="252cc-134">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="252cc-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="252cc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="252cc-135">OUTPUTS</span></span>

### <span data-ttu-id="252cc-136">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="252cc-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="252cc-137">Esse cmdlet retorna a chave de acesso principal e secundária de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="252cc-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="252cc-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="252cc-138">NOTES</span></span>

## <span data-ttu-id="252cc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="252cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="252cc-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="252cc-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


