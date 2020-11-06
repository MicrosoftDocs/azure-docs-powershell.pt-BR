---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24a61f071e806588976f601df69aa66dbbafc164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426098"
---
# <span data-ttu-id="e9e8e-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e8e-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="e9e8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e8e-103">Remove uma política de acesso armazenado de um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="e9e8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9e8e-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e8e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e8e-106">O cmdlet **Remove-AzureStorageShareStoredAccessPolicy** remove uma política de acesso armazenado de um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="e9e8e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e8e-108">Exemplo 1: remover uma política de acesso armazenado de um compartilhamento de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e9e8e-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="e9e8e-109">Esse comando Remove uma política de acesso armazenado chamada GeneralPolicy do ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="e9e8e-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e8e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9e8e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e9e8e-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e9e8e-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e9e8e-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e9e8e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e9e8e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e9e8e-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e9e8e-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e9e8e-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e9e8e-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e9e8e-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e9e8e-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e9e8e-121">-Context</span></span>
<span data-ttu-id="e9e8e-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e9e8e-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e9e8e-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e9e8e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9e8e-124">-PassThru</span></span>
<span data-ttu-id="e9e8e-125">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e9e8e-126">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e9e8e-127">-Política</span><span class="sxs-lookup"><span data-stu-id="e9e8e-127">-Policy</span></span>
<span data-ttu-id="e9e8e-128">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9e8e-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9e8e-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e9e8e-130">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e9e8e-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e9e8e-131">-ShareName</span></span>
<span data-ttu-id="e9e8e-132">Especifica o nome do compartilhamento de armazenamento para o qual esse cmdlet Remove uma política.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="e9e8e-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9e8e-133">-Confirm</span></span>
<span data-ttu-id="e9e8e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e8e-135">-WhatIf</span></span>
<span data-ttu-id="e9e8e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e8e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e8e-138">CommonParameters</span></span>
<span data-ttu-id="e9e8e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e8e-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e8e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e8e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9e8e-141">INPUTS</span></span>

## <span data-ttu-id="e9e8e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9e8e-142">OUTPUTS</span></span>

## <span data-ttu-id="e9e8e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9e8e-143">NOTES</span></span>

## <span data-ttu-id="e9e8e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9e8e-144">RELATED LINKS</span></span>

[<span data-ttu-id="e9e8e-145">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e8e-145">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e9e8e-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e8e-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e9e8e-147">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9e8e-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e9e8e-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e8e-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
