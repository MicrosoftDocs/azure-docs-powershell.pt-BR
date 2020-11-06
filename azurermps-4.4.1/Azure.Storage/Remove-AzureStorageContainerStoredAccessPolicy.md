---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3dbc0f3c014290cb412751440590cbee1f6df685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428335"
---
# <span data-ttu-id="1cd2f-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1cd2f-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="1cd2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd2f-103">Remove uma política de acesso armazenado de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cd2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cd2f-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cd2f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="1cd2f-106">O cmdlet **Remove-AzureStorageContainerStoredAccessPolicy** remove uma política de acesso armazenado de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="1cd2f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cd2f-107">EXAMPLES</span></span>

### <span data-ttu-id="1cd2f-108">Exemplo 1: remover uma política de acesso armazenado de um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1cd2f-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="1cd2f-109">Esse comando Remove uma política de acesso chamada Policy03 do contêiner armazenado chamado mycontainerr.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="1cd2f-110">OS</span><span class="sxs-lookup"><span data-stu-id="1cd2f-110">PARAMETERS</span></span>

### <span data-ttu-id="1cd2f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cd2f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1cd2f-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1cd2f-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1cd2f-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1cd2f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1cd2f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1cd2f-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1cd2f-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1cd2f-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1cd2f-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1cd2f-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="1cd2f-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1cd2f-121">-Container</span></span>
<span data-ttu-id="1cd2f-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd2f-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1cd2f-123">-Context</span></span>
<span data-ttu-id="1cd2f-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1cd2f-125">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1cd2f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cd2f-126">-PassThru</span></span>
<span data-ttu-id="1cd2f-127">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1cd2f-128">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1cd2f-129">-Política</span><span class="sxs-lookup"><span data-stu-id="1cd2f-129">-Policy</span></span>
<span data-ttu-id="1cd2f-130">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd2f-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cd2f-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1cd2f-132">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-132">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1cd2f-133">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-133">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1cd2f-134">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-134">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1cd2f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1cd2f-135">-Confirm</span></span>
<span data-ttu-id="1cd2f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd2f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cd2f-137">-WhatIf</span></span>
<span data-ttu-id="1cd2f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cd2f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd2f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd2f-140">CommonParameters</span></span>
<span data-ttu-id="1cd2f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cd2f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd2f-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd2f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd2f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cd2f-143">INPUTS</span></span>

### <span data-ttu-id="1cd2f-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1cd2f-144">IStorageContext</span></span>

<span data-ttu-id="1cd2f-145">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1cd2f-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="1cd2f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cd2f-146">OUTPUTS</span></span>

### <span data-ttu-id="1cd2f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cd2f-147">System.Boolean</span></span>

## <span data-ttu-id="1cd2f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cd2f-148">NOTES</span></span>

## <span data-ttu-id="1cd2f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cd2f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1cd2f-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1cd2f-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="1cd2f-151">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1cd2f-151">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="1cd2f-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1cd2f-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1cd2f-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1cd2f-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)
