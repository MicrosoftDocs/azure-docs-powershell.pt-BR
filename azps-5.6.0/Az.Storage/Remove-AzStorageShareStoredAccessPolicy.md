---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 9a6702b59bbe2e0305966cd9a1323edc120e86c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886541"
---
# <span data-ttu-id="b2105-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b2105-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b2105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2105-102">SYNOPSIS</span></span>
<span data-ttu-id="b2105-103">Remove uma política de acesso armazenada de um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2105-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="b2105-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2105-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2105-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2105-105">DESCRIPTION</span></span>
<span data-ttu-id="b2105-106">O cmdlet **Remove-AzStorageShareStoredAccessPolicy** remove uma política de acesso armazenada de um compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2105-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="b2105-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2105-107">EXAMPLES</span></span>

### <span data-ttu-id="b2105-108">Exemplo 1: Remover uma política de acesso armazenado de um compartilhamento de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="b2105-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="b2105-109">Este comando remove uma política de acesso armazenada chamada GeneralPolicy da ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="b2105-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="b2105-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2105-110">PARAMETERS</span></span>

### <span data-ttu-id="b2105-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2105-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b2105-112">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b2105-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b2105-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b2105-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b2105-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b2105-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b2105-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b2105-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b2105-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b2105-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b2105-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b2105-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b2105-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="b2105-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b2105-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b2105-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b2105-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="b2105-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b2105-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b2105-121">-Context</span></span>
<span data-ttu-id="b2105-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2105-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b2105-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="b2105-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b2105-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2105-124">-DefaultProfile</span></span>
<span data-ttu-id="b2105-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2105-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2105-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2105-126">-PassThru</span></span>
<span data-ttu-id="b2105-127">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="b2105-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b2105-128">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b2105-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b2105-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="b2105-129">-Policy</span></span>
<span data-ttu-id="b2105-130">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="b2105-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b2105-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2105-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b2105-132">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="b2105-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b2105-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b2105-133">-ShareName</span></span>
<span data-ttu-id="b2105-134">Especifica o nome de compartilhamento de armazenamento para o qual este cmdlet remove uma política.</span><span class="sxs-lookup"><span data-stu-id="b2105-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="b2105-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2105-135">-Confirm</span></span>
<span data-ttu-id="b2105-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2105-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2105-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2105-137">-WhatIf</span></span>
<span data-ttu-id="b2105-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2105-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2105-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2105-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2105-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2105-140">CommonParameters</span></span>
<span data-ttu-id="b2105-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2105-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2105-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2105-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2105-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2105-143">INPUTS</span></span>

### <span data-ttu-id="b2105-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b2105-144">System.String</span></span>

### <span data-ttu-id="b2105-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2105-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b2105-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2105-146">OUTPUTS</span></span>

### <span data-ttu-id="b2105-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2105-147">System.Boolean</span></span>

## <span data-ttu-id="b2105-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2105-148">NOTES</span></span>

## <span data-ttu-id="b2105-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2105-149">RELATED LINKS</span></span>

[<span data-ttu-id="b2105-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b2105-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b2105-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b2105-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b2105-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2105-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b2105-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b2105-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
