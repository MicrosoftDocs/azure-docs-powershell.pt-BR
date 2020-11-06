---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: b453b47da35addb8a04a19957c148c5ec1929e75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429148"
---
# <span data-ttu-id="0b796-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0b796-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="0b796-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b796-102">SYNOPSIS</span></span>
<span data-ttu-id="0b796-103">Regenera a tecla de acesso de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b796-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b796-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b796-105">DESCRIPTION</span></span>
<span data-ttu-id="0b796-106">O cmdlet **New-AzureRmRedisCacheKey** regenera a tecla de acesso de um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="0b796-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b796-107">EXAMPLES</span></span>

### <span data-ttu-id="0b796-108">Exemplo 1: regenerar uma chave primária</span><span class="sxs-lookup"><span data-stu-id="0b796-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="0b796-109">Esse comando regenera a chave primária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="0b796-110">Exemplo 2: regenerar uma chave secundária</span><span class="sxs-lookup"><span data-stu-id="0b796-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="0b796-111">Esse comando regenera a chave secundária de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="0b796-112">OS</span><span class="sxs-lookup"><span data-stu-id="0b796-112">PARAMETERS</span></span>

### <span data-ttu-id="0b796-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0b796-113">-Force</span></span>
<span data-ttu-id="0b796-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b796-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b796-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0b796-115">-KeyType</span></span>
<span data-ttu-id="0b796-116">Especifica se a chave de acesso primária ou secundária deve ser regerada.</span><span class="sxs-lookup"><span data-stu-id="0b796-116">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="0b796-117">Os valores válidos são: principal, secundário.</span><span class="sxs-lookup"><span data-stu-id="0b796-117">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="0b796-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b796-118">-Name</span></span>
<span data-ttu-id="0b796-119">Especifica o nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-119">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="0b796-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b796-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b796-121">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-121">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="0b796-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b796-122">-Confirm</span></span>
<span data-ttu-id="0b796-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b796-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b796-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b796-124">-WhatIf</span></span>
<span data-ttu-id="0b796-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b796-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b796-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b796-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b796-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b796-127">-DefaultProfile</span></span>
<span data-ttu-id="0b796-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b796-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b796-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b796-129">CommonParameters</span></span>
<span data-ttu-id="0b796-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b796-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b796-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b796-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b796-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b796-132">INPUTS</span></span>

### <span data-ttu-id="0b796-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b796-133">None</span></span>
<span data-ttu-id="0b796-134">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="0b796-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="0b796-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b796-135">OUTPUTS</span></span>

### <span data-ttu-id="0b796-136">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0b796-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="0b796-137">Esse cmdlet retorna a chave de acesso principal e secundária de um cache do Redis.</span><span class="sxs-lookup"><span data-stu-id="0b796-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="0b796-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b796-138">NOTES</span></span>

## <span data-ttu-id="0b796-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b796-139">RELATED LINKS</span></span>

[<span data-ttu-id="0b796-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0b796-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


