---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610232"
---
# <span data-ttu-id="961a7-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="961a7-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="961a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="961a7-102">SYNOPSIS</span></span>
<span data-ttu-id="961a7-103">Define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="961a7-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="961a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="961a7-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="961a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="961a7-105">DESCRIPTION</span></span>
<span data-ttu-id="961a7-106">O cmdlet **set-AzureStorageContainerStoredAccessPolicy** define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="961a7-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="961a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="961a7-107">EXAMPLES</span></span>

### <span data-ttu-id="961a7-108">Exemplo 1: definir uma política de acesso armazenado em um contêiner de armazenamento com permissão completa</span><span class="sxs-lookup"><span data-stu-id="961a7-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="961a7-109">Este comando define uma política de acesso chamada Policy06 para o contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="961a7-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="961a7-110">OS</span><span class="sxs-lookup"><span data-stu-id="961a7-110">PARAMETERS</span></span>

### <span data-ttu-id="961a7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="961a7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="961a7-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="961a7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="961a7-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="961a7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="961a7-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="961a7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="961a7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="961a7-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="961a7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="961a7-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="961a7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="961a7-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="961a7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="961a7-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="961a7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="961a7-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="961a7-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="961a7-121">-Container</span></span>
<span data-ttu-id="961a7-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="961a7-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="961a7-123">-Context</span></span>
<span data-ttu-id="961a7-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="961a7-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="961a7-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="961a7-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="961a7-126">-ExpiryTime</span></span>
<span data-ttu-id="961a7-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="961a7-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="961a7-128">-NoExpiryTime</span></span>
<span data-ttu-id="961a7-129">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="961a7-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="961a7-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="961a7-130">-NoStartTime</span></span>
<span data-ttu-id="961a7-131">Define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="961a7-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="961a7-132">-Permissão</span><span class="sxs-lookup"><span data-stu-id="961a7-132">-Permission</span></span>
<span data-ttu-id="961a7-133">Especifica as permissões na política de acesso armazenado para acessar o contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="961a7-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-134">-Política</span><span class="sxs-lookup"><span data-stu-id="961a7-134">-Policy</span></span>
<span data-ttu-id="961a7-135">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="961a7-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="961a7-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="961a7-137">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="961a7-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="961a7-138">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="961a7-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="961a7-139">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="961a7-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="961a7-140">-StartTime</span></span>
<span data-ttu-id="961a7-141">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="961a7-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="961a7-142">-Confirm</span></span>
<span data-ttu-id="961a7-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="961a7-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="961a7-144">-WhatIf</span></span>
<span data-ttu-id="961a7-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="961a7-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="961a7-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="961a7-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961a7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961a7-147">CommonParameters</span></span>
<span data-ttu-id="961a7-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="961a7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961a7-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="961a7-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961a7-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="961a7-150">INPUTS</span></span>

### <span data-ttu-id="961a7-151">String</span><span class="sxs-lookup"><span data-stu-id="961a7-151">String</span></span>

<span data-ttu-id="961a7-152">O parâmetro ' container ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="961a7-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="961a7-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="961a7-153">IStorageContext</span></span>

<span data-ttu-id="961a7-154">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="961a7-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="961a7-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="961a7-155">OUTPUTS</span></span>

### <span data-ttu-id="961a7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="961a7-156">System.String</span></span>

## <span data-ttu-id="961a7-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="961a7-157">NOTES</span></span>

## <span data-ttu-id="961a7-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="961a7-158">RELATED LINKS</span></span>

[<span data-ttu-id="961a7-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="961a7-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="961a7-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="961a7-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="961a7-161">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="961a7-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="961a7-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="961a7-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
