---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: a4013543cfd96a1aaae591a9f1b1ed4b6da46155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772778"
---
# <span data-ttu-id="f500a-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f500a-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f500a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f500a-102">SYNOPSIS</span></span>
<span data-ttu-id="f500a-103">Cria uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f500a-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="f500a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f500a-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f500a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f500a-105">DESCRIPTION</span></span>
<span data-ttu-id="f500a-106">O cmdlet **New-AzStorageShareStoredAccessPolicy** cria uma política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f500a-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="f500a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f500a-107">EXAMPLES</span></span>

### <span data-ttu-id="f500a-108">Exemplo 1: criar uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f500a-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="f500a-109">Esse comando cria uma política de acesso armazenado que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f500a-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="f500a-110">OS</span><span class="sxs-lookup"><span data-stu-id="f500a-110">PARAMETERS</span></span>

### <span data-ttu-id="f500a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f500a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f500a-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="f500a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f500a-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f500a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f500a-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f500a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f500a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f500a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f500a-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f500a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f500a-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f500a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f500a-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="f500a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f500a-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f500a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f500a-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="f500a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f500a-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f500a-121">-Context</span></span>
<span data-ttu-id="f500a-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f500a-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f500a-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f500a-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f500a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f500a-124">-DefaultProfile</span></span>
<span data-ttu-id="f500a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f500a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f500a-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f500a-126">-ExpiryTime</span></span>
<span data-ttu-id="f500a-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="f500a-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f500a-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="f500a-128">-Permission</span></span>
<span data-ttu-id="f500a-129">Especifica as permissões na política de acesso armazenado para acessar os arquivos ou o compartilhamento de armazenamento abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="f500a-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="f500a-130">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="f500a-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f500a-131">-Política</span><span class="sxs-lookup"><span data-stu-id="f500a-131">-Policy</span></span>
<span data-ttu-id="f500a-132">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="f500a-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="f500a-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f500a-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f500a-134">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f500a-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f500a-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f500a-135">-ShareName</span></span>
<span data-ttu-id="f500a-136">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f500a-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="f500a-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f500a-137">-StartTime</span></span>
<span data-ttu-id="f500a-138">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="f500a-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f500a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f500a-139">CommonParameters</span></span>
<span data-ttu-id="f500a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f500a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f500a-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f500a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f500a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f500a-142">INPUTS</span></span>

### <span data-ttu-id="f500a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f500a-143">System.String</span></span>

### <span data-ttu-id="f500a-144">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f500a-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f500a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f500a-145">OUTPUTS</span></span>

### <span data-ttu-id="f500a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f500a-146">System.String</span></span>

## <span data-ttu-id="f500a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f500a-147">NOTES</span></span>

## <span data-ttu-id="f500a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f500a-148">RELATED LINKS</span></span>

[<span data-ttu-id="f500a-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f500a-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f500a-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f500a-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f500a-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f500a-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f500a-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f500a-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)