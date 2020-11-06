---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: cb39d9800271d68f8ac78ebffc9ed3345209177c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427721"
---
# <span data-ttu-id="90a71-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90a71-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="90a71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90a71-102">SYNOPSIS</span></span>
<span data-ttu-id="90a71-103">Remove uma política de acesso armazenado de um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="90a71-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90a71-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90a71-105">DESCRIPTION</span></span>
<span data-ttu-id="90a71-106">O cmdlet **Remove-AzureStorageShareStoredAccessPolicy** remove uma política de acesso armazenado de um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="90a71-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="90a71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90a71-107">EXAMPLES</span></span>

### <span data-ttu-id="90a71-108">Exemplo 1: remover uma política de acesso armazenado de um compartilhamento de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="90a71-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="90a71-109">Esse comando Remove uma política de acesso armazenado chamada GeneralPolicy do ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="90a71-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="90a71-110">OS</span><span class="sxs-lookup"><span data-stu-id="90a71-110">PARAMETERS</span></span>

### <span data-ttu-id="90a71-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90a71-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90a71-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="90a71-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90a71-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="90a71-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90a71-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="90a71-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="90a71-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90a71-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90a71-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90a71-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90a71-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="90a71-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90a71-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="90a71-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90a71-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="90a71-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90a71-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="90a71-120">The default value is 10.</span></span>

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

### <span data-ttu-id="90a71-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="90a71-121">-Context</span></span>
<span data-ttu-id="90a71-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="90a71-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90a71-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="90a71-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="90a71-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90a71-124">-PassThru</span></span>
<span data-ttu-id="90a71-125">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="90a71-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="90a71-126">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="90a71-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="90a71-127">-Política</span><span class="sxs-lookup"><span data-stu-id="90a71-127">-Policy</span></span>
<span data-ttu-id="90a71-128">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="90a71-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90a71-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90a71-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90a71-130">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="90a71-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="90a71-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="90a71-131">-ShareName</span></span>
<span data-ttu-id="90a71-132">Especifica o nome do compartilhamento de armazenamento para o qual esse cmdlet Remove uma política.</span><span class="sxs-lookup"><span data-stu-id="90a71-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="90a71-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90a71-133">-Confirm</span></span>
<span data-ttu-id="90a71-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a71-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a71-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a71-135">-WhatIf</span></span>
<span data-ttu-id="90a71-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90a71-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a71-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90a71-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a71-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a71-138">CommonParameters</span></span>
<span data-ttu-id="90a71-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a71-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a71-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a71-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a71-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90a71-141">INPUTS</span></span>

### <span data-ttu-id="90a71-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90a71-142">IStorageContext</span></span>

<span data-ttu-id="90a71-143">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="90a71-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="90a71-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90a71-144">OUTPUTS</span></span>

### <span data-ttu-id="90a71-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90a71-145">System.Boolean</span></span>

## <span data-ttu-id="90a71-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90a71-146">NOTES</span></span>

## <span data-ttu-id="90a71-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90a71-147">RELATED LINKS</span></span>

[<span data-ttu-id="90a71-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90a71-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="90a71-149">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90a71-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="90a71-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="90a71-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="90a71-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90a71-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
