---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115757"
---
# <span data-ttu-id="76b23-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76b23-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="76b23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76b23-102">SYNOPSIS</span></span>
<span data-ttu-id="76b23-103">Atualiza uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="76b23-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="76b23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76b23-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76b23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76b23-105">DESCRIPTION</span></span>
<span data-ttu-id="76b23-106">O cmdlet **set-AzStorageShareStoredAccessPolicy** atualiza a política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="76b23-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="76b23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76b23-107">EXAMPLES</span></span>

### <span data-ttu-id="76b23-108">Exemplo 1: atualizar uma política de acesso armazenado no compartilhamento de armazenamento</span><span class="sxs-lookup"><span data-stu-id="76b23-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="76b23-109">Esse comando atualiza uma política de acesso armazenada que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="76b23-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="76b23-110">OS</span><span class="sxs-lookup"><span data-stu-id="76b23-110">PARAMETERS</span></span>

### <span data-ttu-id="76b23-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="76b23-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="76b23-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="76b23-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="76b23-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="76b23-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="76b23-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="76b23-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="76b23-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="76b23-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="76b23-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="76b23-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="76b23-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="76b23-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="76b23-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="76b23-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="76b23-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="76b23-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="76b23-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="76b23-120">The default value is 10.</span></span>

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

### <span data-ttu-id="76b23-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="76b23-121">-Context</span></span>
<span data-ttu-id="76b23-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="76b23-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="76b23-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="76b23-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="76b23-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b23-124">-DefaultProfile</span></span>
<span data-ttu-id="76b23-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76b23-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b23-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="76b23-126">-ExpiryTime</span></span>
<span data-ttu-id="76b23-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="76b23-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="76b23-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="76b23-128">-NoExpiryTime</span></span>
<span data-ttu-id="76b23-129">Indica que esse cmdlet limpa a propriedade **ExpiryTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="76b23-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="76b23-130">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="76b23-130">-NoStartTime</span></span>
<span data-ttu-id="76b23-131">Indica que esse cmdlet limpa a propriedade **StartTime** na política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="76b23-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="76b23-132">-Permissão</span><span class="sxs-lookup"><span data-stu-id="76b23-132">-Permission</span></span>
<span data-ttu-id="76b23-133">Especifica as permissões na política de acesso armazenado para acessar o compartilhamento ou arquivos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="76b23-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="76b23-134">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="76b23-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="76b23-135">-Política</span><span class="sxs-lookup"><span data-stu-id="76b23-135">-Policy</span></span>
<span data-ttu-id="76b23-136">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="76b23-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="76b23-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="76b23-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="76b23-138">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="76b23-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="76b23-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="76b23-139">-ShareName</span></span>
<span data-ttu-id="76b23-140">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="76b23-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="76b23-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="76b23-141">-StartTime</span></span>
<span data-ttu-id="76b23-142">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="76b23-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="76b23-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76b23-143">-Confirm</span></span>
<span data-ttu-id="76b23-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76b23-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b23-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b23-145">-WhatIf</span></span>
<span data-ttu-id="76b23-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76b23-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76b23-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76b23-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b23-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b23-148">CommonParameters</span></span>
<span data-ttu-id="76b23-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b23-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b23-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b23-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b23-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76b23-151">INPUTS</span></span>

### <span data-ttu-id="76b23-152">System. String</span><span class="sxs-lookup"><span data-stu-id="76b23-152">System.String</span></span>

### <span data-ttu-id="76b23-153">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="76b23-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="76b23-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76b23-154">OUTPUTS</span></span>

### <span data-ttu-id="76b23-155">System. String</span><span class="sxs-lookup"><span data-stu-id="76b23-155">System.String</span></span>

## <span data-ttu-id="76b23-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76b23-156">NOTES</span></span>

## <span data-ttu-id="76b23-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76b23-157">RELATED LINKS</span></span>

[<span data-ttu-id="76b23-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76b23-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="76b23-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="76b23-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="76b23-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76b23-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="76b23-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76b23-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
