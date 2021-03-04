---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: e2d408e54aa4b4e2de766d4f4e058d2edd22cb22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887654"
---
# <span data-ttu-id="a0405-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0405-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="a0405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0405-102">SYNOPSIS</span></span>
<span data-ttu-id="a0405-103">Remove o contêiner de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="a0405-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="a0405-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a0405-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0405-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a0405-105">DESCRIPTION</span></span>
<span data-ttu-id="a0405-106">O cmdlet **Remove-AzStorageContainer** remove o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="a0405-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="a0405-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0405-107">EXAMPLES</span></span>

### <span data-ttu-id="a0405-108">Exemplo 1: Remover um contêiner</span><span class="sxs-lookup"><span data-stu-id="a0405-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="a0405-109">Este exemplo remove um contêiner chamado MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="a0405-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="a0405-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a0405-110">PARAMETERS</span></span>

### <span data-ttu-id="a0405-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0405-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0405-112">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="a0405-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0405-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a0405-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0405-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a0405-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0405-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0405-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0405-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a0405-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0405-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a0405-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0405-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="a0405-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0405-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a0405-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0405-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a0405-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a0405-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a0405-121">-Context</span></span>
<span data-ttu-id="a0405-122">Especifica um contexto para o contêiner que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="a0405-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="a0405-123">Você pode usar o cmdlet New-AzStorageContext para cria-lo.</span><span class="sxs-lookup"><span data-stu-id="a0405-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="a0405-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0405-124">-DefaultProfile</span></span>
<span data-ttu-id="a0405-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0405-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0405-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a0405-126">-Force</span></span>
<span data-ttu-id="a0405-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0405-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0405-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a0405-128">-Name</span></span>
<span data-ttu-id="a0405-129">Especifica o nome do contêiner a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a0405-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0405-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0405-130">-PassThru</span></span>
<span data-ttu-id="a0405-131">Indica que esse cmdlet retorna um **Boolean** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="a0405-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a0405-132">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a0405-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a0405-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0405-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0405-134">Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="a0405-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a0405-135">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a0405-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a0405-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0405-136">-Confirm</span></span>
<span data-ttu-id="a0405-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0405-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0405-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0405-138">-WhatIf</span></span>
<span data-ttu-id="a0405-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0405-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0405-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0405-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0405-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0405-141">CommonParameters</span></span>
<span data-ttu-id="a0405-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0405-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0405-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0405-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0405-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0405-144">INPUTS</span></span>

### <span data-ttu-id="a0405-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a0405-145">System.String</span></span>

### <span data-ttu-id="a0405-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0405-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0405-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a0405-147">OUTPUTS</span></span>

### <span data-ttu-id="a0405-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0405-148">System.Boolean</span></span>

## <span data-ttu-id="a0405-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="a0405-149">NOTES</span></span>

## <span data-ttu-id="a0405-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0405-150">RELATED LINKS</span></span>

[<span data-ttu-id="a0405-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0405-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="a0405-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a0405-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
