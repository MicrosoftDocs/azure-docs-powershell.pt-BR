---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601808"
---
# <span data-ttu-id="48c8c-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48c8c-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="48c8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="48c8c-103">Cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="48c8c-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="48c8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48c8c-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48c8c-105">DESCRIPTION</span></span>
<span data-ttu-id="48c8c-106">O cmdlet **New-AzureStorageContainerStoredAccessPolicy** cria uma política de acesso armazenado para um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="48c8c-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="48c8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48c8c-107">EXAMPLES</span></span>

### <span data-ttu-id="48c8c-108">Exemplo 1: criar uma política de acesso armazenada em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="48c8c-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="48c8c-109">Esse comando cria uma política de acesso chamada Policy01 no contêiner de armazenamento denominado MyContainer.</span><span class="sxs-lookup"><span data-stu-id="48c8c-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="48c8c-110">OS</span><span class="sxs-lookup"><span data-stu-id="48c8c-110">PARAMETERS</span></span>

### <span data-ttu-id="48c8c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="48c8c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="48c8c-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="48c8c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="48c8c-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="48c8c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="48c8c-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="48c8c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="48c8c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="48c8c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="48c8c-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="48c8c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="48c8c-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="48c8c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="48c8c-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="48c8c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="48c8c-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="48c8c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="48c8c-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="48c8c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="48c8c-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="48c8c-121">-Container</span></span>
<span data-ttu-id="48c8c-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="48c8c-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="48c8c-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="48c8c-123">-Context</span></span>
<span data-ttu-id="48c8c-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="48c8c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="48c8c-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="48c8c-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="48c8c-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="48c8c-126">-ExpiryTime</span></span>
<span data-ttu-id="48c8c-127">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="48c8c-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="48c8c-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="48c8c-128">-Permission</span></span>
<span data-ttu-id="48c8c-129">Especifica o nível de acesso público a este contêiner.</span><span class="sxs-lookup"><span data-stu-id="48c8c-129">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="48c8c-130">-Política</span><span class="sxs-lookup"><span data-stu-id="48c8c-130">-Policy</span></span>
<span data-ttu-id="48c8c-131">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="48c8c-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="48c8c-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="48c8c-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="48c8c-133">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="48c8c-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="48c8c-134">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="48c8c-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="48c8c-135">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="48c8c-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="48c8c-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="48c8c-136">-StartTime</span></span>
<span data-ttu-id="48c8c-137">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="48c8c-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="48c8c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c8c-138">CommonParameters</span></span>
<span data-ttu-id="48c8c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c8c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c8c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c8c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c8c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48c8c-141">INPUTS</span></span>

## <span data-ttu-id="48c8c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48c8c-142">OUTPUTS</span></span>

## <span data-ttu-id="48c8c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48c8c-143">NOTES</span></span>

## <span data-ttu-id="48c8c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48c8c-144">RELATED LINKS</span></span>

[<span data-ttu-id="48c8c-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48c8c-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="48c8c-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="48c8c-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="48c8c-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48c8c-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="48c8c-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48c8c-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


