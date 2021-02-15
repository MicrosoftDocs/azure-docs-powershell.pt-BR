---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116101"
---
# <span data-ttu-id="14879-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14879-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="14879-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14879-102">SYNOPSIS</span></span>
<span data-ttu-id="14879-103">Cria uma política de acesso armazenada em um compartilhamento de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14879-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="14879-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14879-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="14879-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="14879-105">DESCRIPTION</span></span>
<span data-ttu-id="14879-106">O cmdlet **New-AzStorageShareStoredAccessPolicy** cria uma política de acesso armazenada em um compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="14879-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="14879-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14879-107">EXAMPLES</span></span>

### <span data-ttu-id="14879-108">Exemplo 1: Criar uma política de acesso armazenada em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="14879-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="14879-109">Esse comando cria uma política de acesso armazenada que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="14879-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="14879-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14879-110">PARAMETERS</span></span>

### <span data-ttu-id="14879-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14879-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="14879-112">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="14879-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="14879-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="14879-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="14879-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="14879-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="14879-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="14879-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="14879-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="14879-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="14879-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="14879-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="14879-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="14879-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="14879-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="14879-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="14879-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="14879-120">The default value is 10.</span></span>

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

### <span data-ttu-id="14879-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="14879-121">-Context</span></span>
<span data-ttu-id="14879-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="14879-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="14879-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="14879-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="14879-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14879-124">-DefaultProfile</span></span>
<span data-ttu-id="14879-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14879-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14879-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="14879-126">-ExpiryTime</span></span>
<span data-ttu-id="14879-127">Especifica o momento em que a política de acesso armazenada se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="14879-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="14879-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="14879-128">-Permission</span></span>
<span data-ttu-id="14879-129">Especifica permissões na política de acesso armazenada para acessar o compartilhamento de armazenamento ou arquivos sob ela.</span><span class="sxs-lookup"><span data-stu-id="14879-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="14879-130">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="14879-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="14879-131">-Política</span><span class="sxs-lookup"><span data-stu-id="14879-131">-Policy</span></span>
<span data-ttu-id="14879-132">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="14879-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="14879-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14879-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="14879-134">Especifica a duração do período de tempo de tempo para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="14879-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="14879-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="14879-135">-ShareName</span></span>
<span data-ttu-id="14879-136">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14879-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="14879-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="14879-137">-StartTime</span></span>
<span data-ttu-id="14879-138">Especifica o momento em que a política de acesso armazenada se torna válida.</span><span class="sxs-lookup"><span data-stu-id="14879-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="14879-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14879-139">CommonParameters</span></span>
<span data-ttu-id="14879-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14879-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14879-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14879-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14879-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="14879-142">INPUTS</span></span>

### <span data-ttu-id="14879-143">System.String</span><span class="sxs-lookup"><span data-stu-id="14879-143">System.String</span></span>

### <span data-ttu-id="14879-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14879-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14879-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="14879-145">OUTPUTS</span></span>

### <span data-ttu-id="14879-146">System.String</span><span class="sxs-lookup"><span data-stu-id="14879-146">System.String</span></span>

## <span data-ttu-id="14879-147">Notas</span><span class="sxs-lookup"><span data-stu-id="14879-147">NOTES</span></span>

## <span data-ttu-id="14879-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14879-148">RELATED LINKS</span></span>

[<span data-ttu-id="14879-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14879-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="14879-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="14879-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="14879-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14879-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="14879-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14879-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
