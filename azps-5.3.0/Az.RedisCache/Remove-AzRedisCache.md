---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427423"
---
# <span data-ttu-id="35fb8-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="35fb8-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="35fb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="35fb8-103">Remove um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="35fb8-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="35fb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35fb8-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35fb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="35fb8-106">O cmdlet **Remove-AzRedisCache** remove um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="35fb8-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="35fb8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="35fb8-108">Exemplo 1: remover um cache Redis e retornar o resultado</span><span class="sxs-lookup"><span data-stu-id="35fb8-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="35fb8-109">Esse comando Remove um cache Redis e exibe se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="35fb8-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="35fb8-110">Exemplo 2: remover um cache do Redis e não exibir o resultado</span><span class="sxs-lookup"><span data-stu-id="35fb8-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="35fb8-111">Esse comando Remove um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="35fb8-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="35fb8-112">Como o parâmetro *PassThru* não é especificado, o resultado da operação não é exibido.</span><span class="sxs-lookup"><span data-stu-id="35fb8-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="35fb8-113">OS</span><span class="sxs-lookup"><span data-stu-id="35fb8-113">PARAMETERS</span></span>

### <span data-ttu-id="35fb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fb8-114">-DefaultProfile</span></span>
<span data-ttu-id="35fb8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35fb8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35fb8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35fb8-116">-Force</span></span>
<span data-ttu-id="35fb8-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="35fb8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35fb8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="35fb8-118">-Name</span></span>
<span data-ttu-id="35fb8-119">Especifica o nome do cache Redis a ser removido.</span><span class="sxs-lookup"><span data-stu-id="35fb8-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="35fb8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35fb8-120">-PassThru</span></span>
<span data-ttu-id="35fb8-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="35fb8-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35fb8-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="35fb8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35fb8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35fb8-123">-ResourceGroupName</span></span>
<span data-ttu-id="35fb8-124">Especifica o nome do grupo de recursos que contém o cache Redis a ser removido.</span><span class="sxs-lookup"><span data-stu-id="35fb8-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="35fb8-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35fb8-125">-Confirm</span></span>
<span data-ttu-id="35fb8-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fb8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35fb8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35fb8-127">-WhatIf</span></span>
<span data-ttu-id="35fb8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35fb8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35fb8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35fb8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35fb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fb8-130">CommonParameters</span></span>
<span data-ttu-id="35fb8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fb8-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35fb8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fb8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35fb8-133">INPUTS</span></span>

### <span data-ttu-id="35fb8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="35fb8-134">System.String</span></span>

## <span data-ttu-id="35fb8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35fb8-135">OUTPUTS</span></span>

### <span data-ttu-id="35fb8-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35fb8-136">System.Boolean</span></span>

## <span data-ttu-id="35fb8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35fb8-137">NOTES</span></span>

## <span data-ttu-id="35fb8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35fb8-138">RELATED LINKS</span></span>

[<span data-ttu-id="35fb8-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="35fb8-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="35fb8-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="35fb8-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="35fb8-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="35fb8-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


