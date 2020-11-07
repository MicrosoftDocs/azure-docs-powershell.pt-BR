---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 73fc2f9cc72fd56b52851adab31066573c969600
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776160"
---
# <span data-ttu-id="d989b-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d989b-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d989b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d989b-102">SYNOPSIS</span></span>
<span data-ttu-id="d989b-103">Define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d989b-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d989b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d989b-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d989b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d989b-105">DESCRIPTION</span></span>
<span data-ttu-id="d989b-106">O cmdlet **set-AzStorageContainerStoredAccessPolicy** define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d989b-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="d989b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d989b-107">EXAMPLES</span></span>

### <span data-ttu-id="d989b-108">Exemplo 1: definir uma política de acesso armazenado em um contêiner de armazenamento com permissão completa</span><span class="sxs-lookup"><span data-stu-id="d989b-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="d989b-109">Este comando define uma política de acesso chamada Policy06 para o contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="d989b-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="d989b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d989b-110">PARAMETERS</span></span>

### <span data-ttu-id="d989b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d989b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d989b-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d989b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d989b-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d989b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d989b-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d989b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d989b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d989b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d989b-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d989b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d989b-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="d989b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d989b-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="d989b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d989b-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d989b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d989b-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="d989b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d989b-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d989b-121">-Container</span></span>
<span data-ttu-id="d989b-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d989b-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="d989b-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d989b-123">-Context</span></span>
<span data-ttu-id="d989b-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d989b-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d989b-125">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d989b-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d989b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d989b-126">-DefaultProfile</span></span>
<span data-ttu-id="d989b-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d989b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d989b-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d989b-128">-ExpiryTime</span></span>
<span data-ttu-id="d989b-129">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="d989b-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d989b-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d989b-130">-NoExpiryTime</span></span>
<span data-ttu-id="d989b-131">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="d989b-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d989b-132">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="d989b-132">-NoStartTime</span></span>
<span data-ttu-id="d989b-133">Define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="d989b-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="d989b-134">-Permissão</span><span class="sxs-lookup"><span data-stu-id="d989b-134">-Permission</span></span>
<span data-ttu-id="d989b-135">Especifica as permissões na política de acesso armazenado para acessar o contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d989b-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="d989b-136">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="d989b-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d989b-137">-Política</span><span class="sxs-lookup"><span data-stu-id="d989b-137">-Policy</span></span>
<span data-ttu-id="d989b-138">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="d989b-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="d989b-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d989b-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d989b-140">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="d989b-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d989b-141">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d989b-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d989b-142">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d989b-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d989b-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d989b-143">-StartTime</span></span>
<span data-ttu-id="d989b-144">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="d989b-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d989b-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d989b-145">-Confirm</span></span>
<span data-ttu-id="d989b-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d989b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d989b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d989b-147">-WhatIf</span></span>
<span data-ttu-id="d989b-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d989b-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d989b-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d989b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d989b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d989b-150">CommonParameters</span></span>
<span data-ttu-id="d989b-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d989b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d989b-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d989b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d989b-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d989b-153">INPUTS</span></span>

### <span data-ttu-id="d989b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d989b-154">System.String</span></span>

### <span data-ttu-id="d989b-155">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d989b-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d989b-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d989b-156">OUTPUTS</span></span>

### <span data-ttu-id="d989b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d989b-157">System.String</span></span>

## <span data-ttu-id="d989b-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d989b-158">NOTES</span></span>

## <span data-ttu-id="d989b-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d989b-159">RELATED LINKS</span></span>

[<span data-ttu-id="d989b-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d989b-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d989b-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d989b-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d989b-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d989b-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d989b-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d989b-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)