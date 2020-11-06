---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426209"
---
# <span data-ttu-id="75370-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75370-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="75370-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75370-102">SYNOPSIS</span></span>
<span data-ttu-id="75370-103">Define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75370-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="75370-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75370-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75370-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75370-105">DESCRIPTION</span></span>
<span data-ttu-id="75370-106">O cmdlet **set-AzureStorageContainerStoredAccessPolicy** define uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75370-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="75370-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75370-107">EXAMPLES</span></span>

### <span data-ttu-id="75370-108">Exemplo 1: definir uma política de acesso armazenado em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="75370-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="75370-109">Este comando define uma política de acesso chamada Policy06 para o contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="75370-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="75370-110">OS</span><span class="sxs-lookup"><span data-stu-id="75370-110">PARAMETERS</span></span>

### <span data-ttu-id="75370-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75370-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="75370-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="75370-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="75370-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="75370-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="75370-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="75370-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="75370-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="75370-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="75370-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="75370-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="75370-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="75370-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="75370-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="75370-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="75370-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="75370-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="75370-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="75370-120">The default value is 10.</span></span>

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

### <span data-ttu-id="75370-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="75370-121">-Container</span></span>
<span data-ttu-id="75370-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75370-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="75370-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="75370-123">-Context</span></span>
<span data-ttu-id="75370-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75370-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="75370-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="75370-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="75370-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="75370-126">-ExpiryTime</span></span>
<span data-ttu-id="75370-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="75370-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="75370-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="75370-128">-NoExpiryTime</span></span>
<span data-ttu-id="75370-129">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="75370-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="75370-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="75370-130">-NoStartTime</span></span>
<span data-ttu-id="75370-131">Define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="75370-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="75370-132">-Permissão</span><span class="sxs-lookup"><span data-stu-id="75370-132">-Permission</span></span>
<span data-ttu-id="75370-133">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="75370-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="75370-134">-Política</span><span class="sxs-lookup"><span data-stu-id="75370-134">-Policy</span></span>
<span data-ttu-id="75370-135">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="75370-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="75370-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75370-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="75370-137">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="75370-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="75370-138">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="75370-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="75370-139">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="75370-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="75370-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="75370-140">-StartTime</span></span>
<span data-ttu-id="75370-141">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="75370-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="75370-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75370-142">-Confirm</span></span>
<span data-ttu-id="75370-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75370-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75370-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75370-144">-WhatIf</span></span>
<span data-ttu-id="75370-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75370-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75370-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75370-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75370-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75370-147">CommonParameters</span></span>
<span data-ttu-id="75370-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75370-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75370-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75370-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75370-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75370-150">INPUTS</span></span>

## <span data-ttu-id="75370-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75370-151">OUTPUTS</span></span>

## <span data-ttu-id="75370-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75370-152">NOTES</span></span>

## <span data-ttu-id="75370-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75370-153">RELATED LINKS</span></span>

[<span data-ttu-id="75370-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75370-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="75370-155">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="75370-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="75370-156">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75370-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="75370-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75370-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
