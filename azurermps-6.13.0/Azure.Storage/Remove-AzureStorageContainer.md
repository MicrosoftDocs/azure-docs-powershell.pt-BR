---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
ms.openlocfilehash: 13021d9f22d3d2e350c615884b18245007a4e7a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427360"
---
# <span data-ttu-id="9ed19-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ed19-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="9ed19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ed19-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed19-103">Remove o contêiner de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="9ed19-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ed19-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ed19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ed19-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed19-106">O cmdlet **Remove-AzureStorageContainer** remove o contêiner de armazenamento especificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed19-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="9ed19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ed19-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed19-108">Exemplo 1: remover um contêiner</span><span class="sxs-lookup"><span data-stu-id="9ed19-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="9ed19-109">Este exemplo remove um contêiner chamado MyTestContainer.</span><span class="sxs-lookup"><span data-stu-id="9ed19-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="9ed19-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ed19-110">PARAMETERS</span></span>

### <span data-ttu-id="9ed19-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ed19-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9ed19-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ed19-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9ed19-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9ed19-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9ed19-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9ed19-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9ed19-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9ed19-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9ed19-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9ed19-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9ed19-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9ed19-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9ed19-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="9ed19-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9ed19-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="9ed19-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9ed19-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="9ed19-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9ed19-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9ed19-121">-Context</span></span>
<span data-ttu-id="9ed19-122">Especifica um contexto para o contêiner que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="9ed19-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="9ed19-123">Você pode usar o cmdlet New-AzureStorageContext para criá-lo.</span><span class="sxs-lookup"><span data-stu-id="9ed19-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="9ed19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed19-124">-DefaultProfile</span></span>
<span data-ttu-id="9ed19-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed19-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed19-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9ed19-126">-Force</span></span>
<span data-ttu-id="9ed19-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9ed19-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ed19-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ed19-128">-Name</span></span>
<span data-ttu-id="9ed19-129">Especifica o nome do contêiner a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9ed19-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="9ed19-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ed19-130">-PassThru</span></span>
<span data-ttu-id="9ed19-131">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="9ed19-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9ed19-132">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9ed19-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9ed19-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9ed19-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9ed19-134">Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9ed19-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9ed19-135">Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9ed19-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9ed19-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ed19-136">-Confirm</span></span>
<span data-ttu-id="9ed19-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ed19-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed19-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed19-138">-WhatIf</span></span>
<span data-ttu-id="9ed19-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ed19-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed19-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ed19-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed19-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed19-141">CommonParameters</span></span>
<span data-ttu-id="9ed19-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed19-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed19-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed19-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed19-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ed19-144">INPUTS</span></span>

### <span data-ttu-id="9ed19-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed19-145">System.String</span></span>

### <span data-ttu-id="9ed19-146">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ed19-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9ed19-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ed19-147">OUTPUTS</span></span>

### <span data-ttu-id="9ed19-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ed19-148">System.Boolean</span></span>

## <span data-ttu-id="9ed19-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ed19-149">NOTES</span></span>

## <span data-ttu-id="9ed19-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ed19-150">RELATED LINKS</span></span>

[<span data-ttu-id="9ed19-151">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ed19-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="9ed19-152">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ed19-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)