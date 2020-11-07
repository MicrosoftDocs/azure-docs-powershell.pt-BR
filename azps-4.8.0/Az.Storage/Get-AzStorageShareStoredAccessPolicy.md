---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954540"
---
# <span data-ttu-id="a79bf-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79bf-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="a79bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a79bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a79bf-103">Obtém políticas de acesso armazenadas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a79bf-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="a79bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a79bf-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a79bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a79bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a79bf-106">O cmdlet **Get-AzStorageShareStoredAccessPolicy** tem políticas de acesso armazenadas para um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a79bf-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="a79bf-107">Para obter uma política específica, especifique-a por nome.</span><span class="sxs-lookup"><span data-stu-id="a79bf-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="a79bf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a79bf-108">EXAMPLES</span></span>

### <span data-ttu-id="a79bf-109">Exemplo 1: obter uma política de acesso armazenado em um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="a79bf-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="a79bf-110">Este comando obtém uma política de acesso armazenado chamada GeneralPolicy em ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="a79bf-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="a79bf-111">Exemplo 2: obter todas as políticas de acesso armazenadas no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="a79bf-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="a79bf-112">Esse comando obtém todas as políticas de acesso armazenadas no ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="a79bf-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="a79bf-113">OS</span><span class="sxs-lookup"><span data-stu-id="a79bf-113">PARAMETERS</span></span>

### <span data-ttu-id="a79bf-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a79bf-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a79bf-115">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a79bf-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a79bf-116">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a79bf-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a79bf-117">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a79bf-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a79bf-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a79bf-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a79bf-119">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a79bf-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a79bf-120">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a79bf-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a79bf-121">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a79bf-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a79bf-122">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a79bf-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a79bf-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a79bf-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a79bf-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a79bf-124">-Context</span></span>
<span data-ttu-id="a79bf-125">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a79bf-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a79bf-126">Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a79bf-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a79bf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79bf-127">-DefaultProfile</span></span>
<span data-ttu-id="a79bf-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a79bf-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a79bf-129">-Política</span><span class="sxs-lookup"><span data-stu-id="a79bf-129">-Policy</span></span>
<span data-ttu-id="a79bf-130">Especifica o nome da política de acesso armazenado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a79bf-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a79bf-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a79bf-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a79bf-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a79bf-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a79bf-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a79bf-133">-ShareName</span></span>
<span data-ttu-id="a79bf-134">Especifica o nome do compartilhamento de armazenamento para o qual este cmdlet obtém políticas.</span><span class="sxs-lookup"><span data-stu-id="a79bf-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="a79bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79bf-135">CommonParameters</span></span>
<span data-ttu-id="a79bf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79bf-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79bf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79bf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a79bf-138">INPUTS</span></span>

### <span data-ttu-id="a79bf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a79bf-139">System.String</span></span>

### <span data-ttu-id="a79bf-140">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a79bf-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a79bf-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a79bf-141">OUTPUTS</span></span>

### <span data-ttu-id="a79bf-142">Microsoft. Azure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="a79bf-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="a79bf-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a79bf-143">NOTES</span></span>

## <span data-ttu-id="a79bf-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a79bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="a79bf-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a79bf-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a79bf-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79bf-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a79bf-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79bf-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a79bf-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79bf-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
