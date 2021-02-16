---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118573"
---
# <span data-ttu-id="d77b4-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d77b4-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d77b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d77b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d77b4-103">Define uma política de acesso armazenada para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77b4-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d77b4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d77b4-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d77b4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d77b4-105">DESCRIPTION</span></span>
<span data-ttu-id="d77b4-106">O cmdlet **Set-AzStorageContainerStoredAccessPolicy** define uma política de acesso armazenada para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77b4-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d77b4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d77b4-107">EXAMPLES</span></span>

### <span data-ttu-id="d77b4-108">Exemplo 1: Definir uma política de acesso armazenada em um contêiner de armazenamento com permissão total</span><span class="sxs-lookup"><span data-stu-id="d77b4-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="d77b4-109">Esse comando define uma política de acesso chamada Policy06 para contêiner de armazenamento chamado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="d77b4-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="d77b4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d77b4-110">PARAMETERS</span></span>

### <span data-ttu-id="d77b4-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d77b4-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d77b4-112">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d77b4-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d77b4-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d77b4-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d77b4-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d77b4-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d77b4-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d77b4-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d77b4-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d77b4-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d77b4-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d77b4-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d77b4-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="d77b4-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d77b4-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d77b4-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d77b4-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d77b4-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d77b4-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d77b4-121">-Container</span></span>
<span data-ttu-id="d77b4-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77b4-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d77b4-123">-Context</span></span>
<span data-ttu-id="d77b4-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77b4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d77b4-125">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d77b4-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d77b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77b4-126">-DefaultProfile</span></span>
<span data-ttu-id="d77b4-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d77b4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d77b4-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d77b4-128">-ExpiryTime</span></span>
<span data-ttu-id="d77b4-129">Especifica o momento em que a política de acesso armazenada se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="d77b4-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d77b4-130">-NoExpiryTime</span></span>
<span data-ttu-id="d77b4-131">Indica que a política de acesso não tem data de validade.</span><span class="sxs-lookup"><span data-stu-id="d77b4-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d77b4-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d77b4-132">-NoStartTime</span></span>
<span data-ttu-id="d77b4-133">Define a hora de início a ser $Null.</span><span class="sxs-lookup"><span data-stu-id="d77b4-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="d77b4-134">-Permissão</span><span class="sxs-lookup"><span data-stu-id="d77b4-134">-Permission</span></span>
<span data-ttu-id="d77b4-135">Especifica permissões na política de acesso armazenada para acessar o contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d77b4-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="d77b4-136">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="d77b4-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-137">-Política</span><span class="sxs-lookup"><span data-stu-id="d77b4-137">-Policy</span></span>
<span data-ttu-id="d77b4-138">Especifica o nome da política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="d77b4-138">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d77b4-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d77b4-140">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d77b4-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d77b4-141">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d77b4-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d77b4-142">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d77b4-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d77b4-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d77b4-143">-StartTime</span></span>
<span data-ttu-id="d77b4-144">Especifica o momento em que a política de acesso armazenada se torna válida.</span><span class="sxs-lookup"><span data-stu-id="d77b4-144">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d77b4-145">-Confirm</span></span>
<span data-ttu-id="d77b4-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d77b4-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77b4-147">-WhatIf</span></span>
<span data-ttu-id="d77b4-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d77b4-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d77b4-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d77b4-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77b4-150">CommonParameters</span></span>
<span data-ttu-id="d77b4-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77b4-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d77b4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77b4-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="d77b4-153">INPUTS</span></span>

### <span data-ttu-id="d77b4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d77b4-154">System.String</span></span>

### <span data-ttu-id="d77b4-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d77b4-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d77b4-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="d77b4-156">OUTPUTS</span></span>

### <span data-ttu-id="d77b4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d77b4-157">System.String</span></span>

## <span data-ttu-id="d77b4-158">Notas</span><span class="sxs-lookup"><span data-stu-id="d77b4-158">NOTES</span></span>

## <span data-ttu-id="d77b4-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d77b4-159">RELATED LINKS</span></span>

[<span data-ttu-id="d77b4-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d77b4-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d77b4-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d77b4-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d77b4-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d77b4-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d77b4-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d77b4-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
