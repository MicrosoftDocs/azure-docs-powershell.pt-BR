---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116096"
---
# <span data-ttu-id="b48e9-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b48e9-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b48e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b48e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b48e9-103">Remove uma política de acesso armazenada de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b48e9-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="b48e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b48e9-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b48e9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b48e9-105">DESCRIPTION</span></span>
<span data-ttu-id="b48e9-106">O cmdlet **Remove-AzStorageContainerStoredAccessPolicy** remove uma política de acesso armazenada de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b48e9-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="b48e9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b48e9-107">EXAMPLES</span></span>

### <span data-ttu-id="b48e9-108">Exemplo 1: Remover uma política de acesso armazenada de um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b48e9-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="b48e9-109">Esse comando remove uma política de acesso chamada Policy03 do contêiner armazenado chamado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="b48e9-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="b48e9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b48e9-110">PARAMETERS</span></span>

### <span data-ttu-id="b48e9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b48e9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b48e9-112">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b48e9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b48e9-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b48e9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b48e9-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b48e9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b48e9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b48e9-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b48e9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b48e9-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b48e9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b48e9-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b48e9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b48e9-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b48e9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b48e9-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b48e9-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="b48e9-121">-Container</span></span>
<span data-ttu-id="b48e9-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b48e9-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b48e9-123">-Context</span></span>
<span data-ttu-id="b48e9-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b48e9-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b48e9-125">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b48e9-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48e9-126">-DefaultProfile</span></span>
<span data-ttu-id="b48e9-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b48e9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b48e9-128">-PassThru</span></span>
<span data-ttu-id="b48e9-129">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="b48e9-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b48e9-130">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b48e9-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b48e9-131">-Política</span><span class="sxs-lookup"><span data-stu-id="b48e9-131">-Policy</span></span>
<span data-ttu-id="b48e9-132">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b48e9-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b48e9-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b48e9-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b48e9-134">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b48e9-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b48e9-135">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b48e9-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b48e9-136">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b48e9-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48e9-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b48e9-137">-Confirm</span></span>
<span data-ttu-id="b48e9-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b48e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48e9-139">-WhatIf</span></span>
<span data-ttu-id="b48e9-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b48e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48e9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b48e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48e9-142">CommonParameters</span></span>
<span data-ttu-id="b48e9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48e9-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48e9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48e9-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="b48e9-145">INPUTS</span></span>

### <span data-ttu-id="b48e9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b48e9-146">System.String</span></span>

### <span data-ttu-id="b48e9-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b48e9-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b48e9-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="b48e9-148">OUTPUTS</span></span>

### <span data-ttu-id="b48e9-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b48e9-149">System.Boolean</span></span>

## <span data-ttu-id="b48e9-150">Notas</span><span class="sxs-lookup"><span data-stu-id="b48e9-150">NOTES</span></span>

## <span data-ttu-id="b48e9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b48e9-151">RELATED LINKS</span></span>

[<span data-ttu-id="b48e9-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b48e9-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b48e9-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b48e9-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b48e9-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b48e9-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b48e9-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b48e9-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
