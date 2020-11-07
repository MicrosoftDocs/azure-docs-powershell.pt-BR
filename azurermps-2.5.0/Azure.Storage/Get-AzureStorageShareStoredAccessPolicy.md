---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 5e4a6c5ad69ae8f31564335a410a67ec58181f3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785386"
---
# <span data-ttu-id="cbe5e-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cbe5e-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="cbe5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbe5e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe5e-103">Obtém políticas de acesso armazenadas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbe5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbe5e-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cbe5e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbe5e-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe5e-106">O cmdlet **Get-AzureStorageShareStoredAccessPolicy** tem políticas de acesso armazenadas para um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="cbe5e-107">Para obter uma política específica, especifique-a por nome.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="cbe5e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbe5e-108">EXAMPLES</span></span>

### <span data-ttu-id="cbe5e-109">Exemplo 1: obter uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="cbe5e-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="cbe5e-110">Este comando obtém uma política de acesso armazenado chamada GeneralPolicy em ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="cbe5e-111">Exemplo 2: obter todas as políticas de acesso armazenadas no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="cbe5e-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="cbe5e-112">Esse comando obtém todas as políticas de acesso armazenadas no ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="cbe5e-113">OS</span><span class="sxs-lookup"><span data-stu-id="cbe5e-113">PARAMETERS</span></span>

### <span data-ttu-id="cbe5e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbe5e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cbe5e-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cbe5e-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cbe5e-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cbe5e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cbe5e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cbe5e-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cbe5e-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cbe5e-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cbe5e-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cbe5e-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-123">The default value is 10.</span></span>

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

### <span data-ttu-id="cbe5e-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cbe5e-124">-Context</span></span>
<span data-ttu-id="cbe5e-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cbe5e-126">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cbe5e-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cbe5e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe5e-127">-DefaultProfile</span></span>
<span data-ttu-id="cbe5e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe5e-129">-Política</span><span class="sxs-lookup"><span data-stu-id="cbe5e-129">-Policy</span></span>
<span data-ttu-id="cbe5e-130">Especifica o nome da política de acesso armazenado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe5e-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbe5e-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cbe5e-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cbe5e-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cbe5e-133">-ShareName</span></span>
<span data-ttu-id="cbe5e-134">Especifica o nome do compartilhamento de armazenamento para o qual este cmdlet obtém políticas.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="cbe5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe5e-135">CommonParameters</span></span>
<span data-ttu-id="cbe5e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe5e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe5e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe5e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbe5e-138">INPUTS</span></span>

### <span data-ttu-id="cbe5e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cbe5e-139">System.String</span></span>

### <span data-ttu-id="cbe5e-140">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cbe5e-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cbe5e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbe5e-141">OUTPUTS</span></span>

### <span data-ttu-id="cbe5e-142">Microsoft. WindowsAzure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="cbe5e-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="cbe5e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbe5e-143">NOTES</span></span>

## <span data-ttu-id="cbe5e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbe5e-144">RELATED LINKS</span></span>

[<span data-ttu-id="cbe5e-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cbe5e-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cbe5e-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cbe5e-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="cbe5e-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cbe5e-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="cbe5e-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cbe5e-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
