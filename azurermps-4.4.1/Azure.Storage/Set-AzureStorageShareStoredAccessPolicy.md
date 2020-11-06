---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 43e9ccca185a68d3c7b0e6cca118bb2cd63247bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440243"
---
# <span data-ttu-id="8fda9-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8fda9-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="8fda9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fda9-102">SYNOPSIS</span></span>
<span data-ttu-id="8fda9-103">Atualiza uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8fda9-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fda9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fda9-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fda9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fda9-105">DESCRIPTION</span></span>
<span data-ttu-id="8fda9-106">O cmdlet **set-AzureStorageShareStoredAccessPolicy** atualiza a política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fda9-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="8fda9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fda9-107">EXAMPLES</span></span>

### <span data-ttu-id="8fda9-108">Exemplo 1: atualizar uma política de acesso armazenado no compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8fda9-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="8fda9-109">Esse comando atualiza uma política de acesso armazenada que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="8fda9-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="8fda9-110">OS</span><span class="sxs-lookup"><span data-stu-id="8fda9-110">PARAMETERS</span></span>

### <span data-ttu-id="8fda9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8fda9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8fda9-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fda9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8fda9-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8fda9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8fda9-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8fda9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8fda9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8fda9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8fda9-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8fda9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8fda9-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="8fda9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8fda9-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="8fda9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8fda9-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8fda9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8fda9-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="8fda9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8fda9-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8fda9-121">-Context</span></span>
<span data-ttu-id="8fda9-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fda9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8fda9-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8fda9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8fda9-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8fda9-124">-ExpiryTime</span></span>
<span data-ttu-id="8fda9-125">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="8fda9-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8fda9-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8fda9-126">-NoExpiryTime</span></span>
<span data-ttu-id="8fda9-127">Indica que esse cmdlet limpa a propriedade **ExpiryTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="8fda9-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="8fda9-128">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="8fda9-128">-NoStartTime</span></span>
<span data-ttu-id="8fda9-129">Indica que esse cmdlet limpa a propriedade **StartTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="8fda9-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="8fda9-130">-Permissão</span><span class="sxs-lookup"><span data-stu-id="8fda9-130">-Permission</span></span>
<span data-ttu-id="8fda9-131">Especifica as permissões na política de acesso armazenado para acessar o compartilhamento ou arquivos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="8fda9-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="8fda9-132">-Política</span><span class="sxs-lookup"><span data-stu-id="8fda9-132">-Policy</span></span>
<span data-ttu-id="8fda9-133">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="8fda9-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="8fda9-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8fda9-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8fda9-135">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8fda9-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8fda9-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8fda9-136">-ShareName</span></span>
<span data-ttu-id="8fda9-137">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8fda9-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="8fda9-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8fda9-138">-StartTime</span></span>
<span data-ttu-id="8fda9-139">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="8fda9-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8fda9-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fda9-140">-Confirm</span></span>
<span data-ttu-id="8fda9-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fda9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fda9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fda9-142">-WhatIf</span></span>
<span data-ttu-id="8fda9-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fda9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fda9-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fda9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fda9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fda9-145">CommonParameters</span></span>
<span data-ttu-id="8fda9-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fda9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fda9-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fda9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fda9-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fda9-148">INPUTS</span></span>

### <span data-ttu-id="8fda9-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fda9-149">IStorageContext</span></span>

<span data-ttu-id="8fda9-150">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fda9-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8fda9-151">String</span><span class="sxs-lookup"><span data-stu-id="8fda9-151">String</span></span>

<span data-ttu-id="8fda9-152">O parâmetro ' ShareName ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fda9-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8fda9-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fda9-153">OUTPUTS</span></span>

### <span data-ttu-id="8fda9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8fda9-154">System.String</span></span>

## <span data-ttu-id="8fda9-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fda9-155">NOTES</span></span>

## <span data-ttu-id="8fda9-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fda9-156">RELATED LINKS</span></span>

[<span data-ttu-id="8fda9-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8fda9-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8fda9-158">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fda9-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8fda9-159">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8fda9-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="8fda9-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8fda9-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
