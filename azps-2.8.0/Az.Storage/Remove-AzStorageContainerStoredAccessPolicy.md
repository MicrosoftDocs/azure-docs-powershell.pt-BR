---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: bc4df20e16acbc74b2bb0867beba6d9e65191461
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774230"
---
# <span data-ttu-id="81edb-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81edb-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="81edb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81edb-102">SYNOPSIS</span></span>
<span data-ttu-id="81edb-103">Remove uma política de acesso armazenado de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="81edb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81edb-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81edb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81edb-105">DESCRIPTION</span></span>
<span data-ttu-id="81edb-106">O cmdlet **Remove-AzStorageContainerStoredAccessPolicy** remove uma política de acesso armazenado de um contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="81edb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81edb-107">EXAMPLES</span></span>

### <span data-ttu-id="81edb-108">Exemplo 1: remover uma política de acesso armazenado de um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="81edb-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="81edb-109">Esse comando Remove uma política de acesso chamada Policy03 do contêiner armazenado chamado mycontainerr.</span><span class="sxs-lookup"><span data-stu-id="81edb-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="81edb-110">OS</span><span class="sxs-lookup"><span data-stu-id="81edb-110">PARAMETERS</span></span>

### <span data-ttu-id="81edb-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="81edb-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="81edb-112">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="81edb-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="81edb-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="81edb-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="81edb-114">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="81edb-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="81edb-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="81edb-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="81edb-116">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="81edb-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="81edb-117">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="81edb-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="81edb-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="81edb-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="81edb-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="81edb-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="81edb-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="81edb-120">The default value is 10.</span></span>

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

### <span data-ttu-id="81edb-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="81edb-121">-Container</span></span>
<span data-ttu-id="81edb-122">Especifica o nome do contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81edb-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="81edb-123">-Context</span></span>
<span data-ttu-id="81edb-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="81edb-125">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="81edb-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="81edb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81edb-126">-DefaultProfile</span></span>
<span data-ttu-id="81edb-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81edb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81edb-128">-PassThru</span></span>
<span data-ttu-id="81edb-129">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="81edb-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="81edb-130">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="81edb-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="81edb-131">-Política</span><span class="sxs-lookup"><span data-stu-id="81edb-131">-Policy</span></span>
<span data-ttu-id="81edb-132">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="81edb-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81edb-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="81edb-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="81edb-134">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="81edb-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="81edb-135">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="81edb-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="81edb-136">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="81edb-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="81edb-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81edb-137">-Confirm</span></span>
<span data-ttu-id="81edb-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81edb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81edb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81edb-139">-WhatIf</span></span>
<span data-ttu-id="81edb-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81edb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81edb-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81edb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81edb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81edb-142">CommonParameters</span></span>
<span data-ttu-id="81edb-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81edb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81edb-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81edb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81edb-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81edb-145">INPUTS</span></span>

### <span data-ttu-id="81edb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="81edb-146">System.String</span></span>

### <span data-ttu-id="81edb-147">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="81edb-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="81edb-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81edb-148">OUTPUTS</span></span>

### <span data-ttu-id="81edb-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81edb-149">System.Boolean</span></span>

## <span data-ttu-id="81edb-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81edb-150">NOTES</span></span>

## <span data-ttu-id="81edb-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81edb-151">RELATED LINKS</span></span>

[<span data-ttu-id="81edb-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81edb-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="81edb-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81edb-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="81edb-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="81edb-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="81edb-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81edb-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)