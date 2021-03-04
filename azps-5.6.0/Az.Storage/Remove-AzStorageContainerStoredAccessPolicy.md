---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 4d2828351c4007e57fd8c7534e88aa3be5543199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890343"
---
# <span data-ttu-id="7d97d-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d97d-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="7d97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d97d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d97d-103">Remove uma política de acesso armazenada de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d97d-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="7d97d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d97d-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d97d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d97d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d97d-106">O cmdlet **Remove-AzStorageContainerStoredAccessPolicy** remove uma política de acesso armazenada de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d97d-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="7d97d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d97d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d97d-108">Exemplo 1: Remover uma política de acesso armazenado de um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7d97d-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="7d97d-109">Este comando remove uma política de acesso chamada Policy03 do contêiner armazenado chamado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="7d97d-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="7d97d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d97d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d97d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d97d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7d97d-112">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="7d97d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7d97d-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7d97d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7d97d-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7d97d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d97d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7d97d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7d97d-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7d97d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7d97d-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="7d97d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7d97d-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="7d97d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7d97d-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="7d97d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7d97d-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="7d97d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7d97d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="7d97d-121">-Container</span></span>
<span data-ttu-id="7d97d-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d97d-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="7d97d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="7d97d-123">-Context</span></span>
<span data-ttu-id="7d97d-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d97d-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7d97d-125">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d97d-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7d97d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d97d-126">-DefaultProfile</span></span>
<span data-ttu-id="7d97d-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d97d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d97d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d97d-128">-PassThru</span></span>
<span data-ttu-id="7d97d-129">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="7d97d-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7d97d-130">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7d97d-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7d97d-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="7d97d-131">-Policy</span></span>
<span data-ttu-id="7d97d-132">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="7d97d-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d97d-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d97d-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7d97d-134">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="7d97d-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7d97d-135">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7d97d-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7d97d-136">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7d97d-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d97d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d97d-137">-Confirm</span></span>
<span data-ttu-id="7d97d-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d97d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d97d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d97d-139">-WhatIf</span></span>
<span data-ttu-id="7d97d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d97d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d97d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d97d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d97d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d97d-142">CommonParameters</span></span>
<span data-ttu-id="7d97d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d97d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d97d-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d97d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d97d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d97d-145">INPUTS</span></span>

### <span data-ttu-id="7d97d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7d97d-146">System.String</span></span>

### <span data-ttu-id="7d97d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d97d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7d97d-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d97d-148">OUTPUTS</span></span>

### <span data-ttu-id="7d97d-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d97d-149">System.Boolean</span></span>

## <span data-ttu-id="7d97d-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d97d-150">NOTES</span></span>

## <span data-ttu-id="7d97d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d97d-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d97d-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d97d-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7d97d-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d97d-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="7d97d-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d97d-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7d97d-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d97d-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
