---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429713"
---
# <span data-ttu-id="32afe-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="32afe-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="32afe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32afe-102">SYNOPSIS</span></span>
<span data-ttu-id="32afe-103">Remove um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="32afe-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32afe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32afe-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32afe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32afe-105">DESCRIPTION</span></span>
<span data-ttu-id="32afe-106">O cmdlet **Remove-AzureRmRedisCache** remove um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="32afe-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="32afe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32afe-107">EXAMPLES</span></span>

### <span data-ttu-id="32afe-108">Exemplo 1: remover um cache Redis e retornar o resultado</span><span class="sxs-lookup"><span data-stu-id="32afe-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="32afe-109">Esse comando Remove um cache Redis e exibe se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="32afe-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="32afe-110">Exemplo 2: remover um cache do Redis e não exibir o resultado</span><span class="sxs-lookup"><span data-stu-id="32afe-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="32afe-111">Esse comando Remove um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="32afe-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="32afe-112">Como o parâmetro *PassThru* não é especificado, o resultado da operação não é exibido.</span><span class="sxs-lookup"><span data-stu-id="32afe-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="32afe-113">OS</span><span class="sxs-lookup"><span data-stu-id="32afe-113">PARAMETERS</span></span>

### <span data-ttu-id="32afe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32afe-114">-DefaultProfile</span></span>
<span data-ttu-id="32afe-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32afe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32afe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="32afe-116">-Force</span></span>
<span data-ttu-id="32afe-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="32afe-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32afe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="32afe-118">-Name</span></span>
<span data-ttu-id="32afe-119">Especifica o nome do cache Redis a ser removido.</span><span class="sxs-lookup"><span data-stu-id="32afe-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="32afe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32afe-120">-PassThru</span></span>
<span data-ttu-id="32afe-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="32afe-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32afe-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="32afe-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32afe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32afe-123">-ResourceGroupName</span></span>
<span data-ttu-id="32afe-124">Especifica o nome do grupo de recursos que contém o cache Redis a ser removido.</span><span class="sxs-lookup"><span data-stu-id="32afe-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="32afe-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32afe-125">-Confirm</span></span>
<span data-ttu-id="32afe-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32afe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32afe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32afe-127">-WhatIf</span></span>
<span data-ttu-id="32afe-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32afe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32afe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32afe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32afe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32afe-130">CommonParameters</span></span>
<span data-ttu-id="32afe-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32afe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32afe-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32afe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32afe-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32afe-133">INPUTS</span></span>

### <span data-ttu-id="32afe-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="32afe-134">None</span></span>
<span data-ttu-id="32afe-135">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="32afe-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="32afe-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32afe-136">OUTPUTS</span></span>

### <span data-ttu-id="32afe-137">Booliana</span><span class="sxs-lookup"><span data-stu-id="32afe-137">Boolean</span></span>
<span data-ttu-id="32afe-138">Retorna $True se nenhuma exceção ocorrer.</span><span class="sxs-lookup"><span data-stu-id="32afe-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="32afe-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32afe-139">NOTES</span></span>

## <span data-ttu-id="32afe-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32afe-140">RELATED LINKS</span></span>

[<span data-ttu-id="32afe-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="32afe-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="32afe-142">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="32afe-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="32afe-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="32afe-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


