---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86ce98b1ec4d77ffc82ba923b5709321f3b3b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426203"
---
# <span data-ttu-id="ab182-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab182-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="ab182-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab182-102">SYNOPSIS</span></span>
<span data-ttu-id="ab182-103">Atualiza uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ab182-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="ab182-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab182-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab182-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab182-105">DESCRIPTION</span></span>
<span data-ttu-id="ab182-106">O cmdlet **set-AzureStorageShareStoredAccessPolicy** atualiza a política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab182-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="ab182-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab182-107">EXAMPLES</span></span>

### <span data-ttu-id="ab182-108">Exemplo 1: atualizar uma política de acesso armazenado no compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ab182-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="ab182-109">Esse comando atualiza uma política de acesso armazenada que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ab182-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="ab182-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab182-110">PARAMETERS</span></span>

### <span data-ttu-id="ab182-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab182-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ab182-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab182-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ab182-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ab182-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ab182-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ab182-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ab182-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ab182-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ab182-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ab182-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ab182-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ab182-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ab182-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="ab182-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ab182-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ab182-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ab182-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="ab182-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ab182-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ab182-121">-Context</span></span>
<span data-ttu-id="ab182-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab182-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ab182-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ab182-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ab182-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ab182-124">-ExpiryTime</span></span>
<span data-ttu-id="ab182-125">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="ab182-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ab182-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ab182-126">-NoExpiryTime</span></span>
<span data-ttu-id="ab182-127">Indica que esse cmdlet limpa a propriedade **ExpiryTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="ab182-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ab182-128">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="ab182-128">-NoStartTime</span></span>
<span data-ttu-id="ab182-129">Indica que esse cmdlet limpa a propriedade **StartTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="ab182-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ab182-130">-Permissão</span><span class="sxs-lookup"><span data-stu-id="ab182-130">-Permission</span></span>
<span data-ttu-id="ab182-131">Especifica as permissões na política de acesso armazenado para acessar o compartilhamento ou arquivos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="ab182-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="ab182-132">-Política</span><span class="sxs-lookup"><span data-stu-id="ab182-132">-Policy</span></span>
<span data-ttu-id="ab182-133">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="ab182-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="ab182-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab182-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ab182-135">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="ab182-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ab182-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ab182-136">-ShareName</span></span>
<span data-ttu-id="ab182-137">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ab182-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="ab182-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ab182-138">-StartTime</span></span>
<span data-ttu-id="ab182-139">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="ab182-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ab182-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab182-140">-Confirm</span></span>
<span data-ttu-id="ab182-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab182-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab182-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab182-142">-WhatIf</span></span>
<span data-ttu-id="ab182-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab182-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab182-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab182-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab182-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab182-145">CommonParameters</span></span>
<span data-ttu-id="ab182-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab182-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab182-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab182-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab182-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab182-148">INPUTS</span></span>

## <span data-ttu-id="ab182-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab182-149">OUTPUTS</span></span>

## <span data-ttu-id="ab182-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab182-150">NOTES</span></span>

## <span data-ttu-id="ab182-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab182-151">RELATED LINKS</span></span>

[<span data-ttu-id="ab182-152">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab182-152">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ab182-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab182-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ab182-154">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab182-154">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ab182-155">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab182-155">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
