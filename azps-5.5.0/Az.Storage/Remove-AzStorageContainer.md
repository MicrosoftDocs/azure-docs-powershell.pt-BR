---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118577"
---
# <span data-ttu-id="eecbc-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eecbc-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="eecbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eecbc-102">SYNOPSIS</span></span>
<span data-ttu-id="eecbc-103">Remove o contêiner de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="eecbc-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="eecbc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eecbc-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eecbc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eecbc-105">DESCRIPTION</span></span>
<span data-ttu-id="eecbc-106">O cmdlet **Remove-AzStorageContainer** remove o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="eecbc-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="eecbc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eecbc-107">EXAMPLES</span></span>

### <span data-ttu-id="eecbc-108">Exemplo 1: Remover um contêiner</span><span class="sxs-lookup"><span data-stu-id="eecbc-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="eecbc-109">Este exemplo remove um contêiner chamado MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="eecbc-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="eecbc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eecbc-110">PARAMETERS</span></span>

### <span data-ttu-id="eecbc-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eecbc-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eecbc-112">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="eecbc-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eecbc-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="eecbc-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eecbc-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="eecbc-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eecbc-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eecbc-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eecbc-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="eecbc-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eecbc-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="eecbc-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eecbc-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="eecbc-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eecbc-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="eecbc-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eecbc-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="eecbc-120">The default value is 10.</span></span>

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

### <span data-ttu-id="eecbc-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="eecbc-121">-Context</span></span>
<span data-ttu-id="eecbc-122">Especifica um contexto para o contêiner que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="eecbc-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="eecbc-123">Você pode usar o cmdlet New-AzStorageContext para criar.</span><span class="sxs-lookup"><span data-stu-id="eecbc-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="eecbc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eecbc-124">-DefaultProfile</span></span>
<span data-ttu-id="eecbc-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eecbc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eecbc-126">-Forçar</span><span class="sxs-lookup"><span data-stu-id="eecbc-126">-Force</span></span>
<span data-ttu-id="eecbc-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="eecbc-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eecbc-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="eecbc-128">-Name</span></span>
<span data-ttu-id="eecbc-129">Especifica o nome do contêiner a ser removido.</span><span class="sxs-lookup"><span data-stu-id="eecbc-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="eecbc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eecbc-130">-PassThru</span></span>
<span data-ttu-id="eecbc-131">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="eecbc-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eecbc-132">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eecbc-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eecbc-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eecbc-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eecbc-134">Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="eecbc-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="eecbc-135">Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="eecbc-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="eecbc-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eecbc-136">-Confirm</span></span>
<span data-ttu-id="eecbc-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eecbc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eecbc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eecbc-138">-WhatIf</span></span>
<span data-ttu-id="eecbc-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eecbc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eecbc-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eecbc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eecbc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eecbc-141">CommonParameters</span></span>
<span data-ttu-id="eecbc-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eecbc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eecbc-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eecbc-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eecbc-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="eecbc-144">INPUTS</span></span>

### <span data-ttu-id="eecbc-145">System.String</span><span class="sxs-lookup"><span data-stu-id="eecbc-145">System.String</span></span>

### <span data-ttu-id="eecbc-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eecbc-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eecbc-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="eecbc-147">OUTPUTS</span></span>

### <span data-ttu-id="eecbc-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eecbc-148">System.Boolean</span></span>

## <span data-ttu-id="eecbc-149">Notas</span><span class="sxs-lookup"><span data-stu-id="eecbc-149">NOTES</span></span>

## <span data-ttu-id="eecbc-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eecbc-150">RELATED LINKS</span></span>

[<span data-ttu-id="eecbc-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eecbc-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="eecbc-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eecbc-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
