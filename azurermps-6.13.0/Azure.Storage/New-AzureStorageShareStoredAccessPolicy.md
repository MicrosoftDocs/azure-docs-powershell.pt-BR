---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 823ae6183021e368933af8d2e01a61f0b582323e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428661"
---
# <span data-ttu-id="705c1-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="705c1-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="705c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="705c1-102">SYNOPSIS</span></span>
<span data-ttu-id="705c1-103">Cria uma política de acesso armazenado em um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="705c1-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="705c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="705c1-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="705c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="705c1-105">DESCRIPTION</span></span>
<span data-ttu-id="705c1-106">O cmdlet **New-AzureStorageShareStoredAccessPolicy** cria uma política de acesso armazenado em um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="705c1-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="705c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="705c1-107">EXAMPLES</span></span>

### <span data-ttu-id="705c1-108">Exemplo 1: criar uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="705c1-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="705c1-109">Esse comando cria uma política de acesso armazenado que tem permissão total em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="705c1-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="705c1-110">OS</span><span class="sxs-lookup"><span data-stu-id="705c1-110">PARAMETERS</span></span>

### <span data-ttu-id="705c1-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="705c1-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="705c1-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="705c1-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="705c1-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="705c1-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="705c1-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="705c1-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="705c1-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="705c1-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="705c1-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="705c1-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="705c1-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="705c1-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="705c1-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="705c1-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="705c1-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="705c1-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="705c1-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="705c1-120">The default value is 10.</span></span>

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

### <span data-ttu-id="705c1-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="705c1-121">-Context</span></span>
<span data-ttu-id="705c1-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="705c1-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="705c1-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="705c1-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="705c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705c1-124">-DefaultProfile</span></span>
<span data-ttu-id="705c1-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="705c1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="705c1-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="705c1-126">-ExpiryTime</span></span>
<span data-ttu-id="705c1-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="705c1-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="705c1-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="705c1-128">-Permission</span></span>
<span data-ttu-id="705c1-129">Especifica as permissões na política de acesso armazenado para acessar os arquivos ou o compartilhamento de armazenamento abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="705c1-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="705c1-130">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="705c1-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="705c1-131">-Política</span><span class="sxs-lookup"><span data-stu-id="705c1-131">-Policy</span></span>
<span data-ttu-id="705c1-132">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="705c1-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="705c1-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="705c1-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="705c1-134">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="705c1-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="705c1-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="705c1-135">-ShareName</span></span>
<span data-ttu-id="705c1-136">Especifica o nome do compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="705c1-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="705c1-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="705c1-137">-StartTime</span></span>
<span data-ttu-id="705c1-138">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="705c1-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="705c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705c1-139">CommonParameters</span></span>
<span data-ttu-id="705c1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705c1-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705c1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705c1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="705c1-142">INPUTS</span></span>

### <span data-ttu-id="705c1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="705c1-143">System.String</span></span>

### <span data-ttu-id="705c1-144">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="705c1-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="705c1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="705c1-145">OUTPUTS</span></span>

### <span data-ttu-id="705c1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="705c1-146">System.String</span></span>

## <span data-ttu-id="705c1-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="705c1-147">NOTES</span></span>

## <span data-ttu-id="705c1-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="705c1-148">RELATED LINKS</span></span>

[<span data-ttu-id="705c1-149">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="705c1-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="705c1-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="705c1-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="705c1-151">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="705c1-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="705c1-152">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="705c1-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
