---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114405"
---
# <span data-ttu-id="62399-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62399-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="62399-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62399-102">SYNOPSIS</span></span>
<span data-ttu-id="62399-103">Remove uma política de acesso armazenada de um compartilhamento de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62399-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="62399-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62399-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62399-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="62399-105">DESCRIPTION</span></span>
<span data-ttu-id="62399-106">O cmdlet **Remove-AzStorageShareStoredAccessPolicy** remove uma política de acesso armazenada de um compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="62399-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="62399-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62399-107">EXAMPLES</span></span>

### <span data-ttu-id="62399-108">Exemplo 1: Remover uma política de acesso armazenada de um compartilhamento de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="62399-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="62399-109">Esse comando remove uma política de acesso armazenada chamada GeneralPolicy da ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="62399-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="62399-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62399-110">PARAMETERS</span></span>

### <span data-ttu-id="62399-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62399-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="62399-112">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="62399-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="62399-113">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="62399-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="62399-114">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="62399-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="62399-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="62399-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="62399-116">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="62399-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="62399-117">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="62399-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="62399-118">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="62399-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="62399-119">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="62399-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="62399-120">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="62399-120">The default value is 10.</span></span>

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

### <span data-ttu-id="62399-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="62399-121">-Context</span></span>
<span data-ttu-id="62399-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="62399-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="62399-123">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="62399-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="62399-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62399-124">-DefaultProfile</span></span>
<span data-ttu-id="62399-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62399-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62399-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62399-126">-PassThru</span></span>
<span data-ttu-id="62399-127">Indica que esse cmdlet retorna um **boolano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="62399-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="62399-128">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="62399-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="62399-129">-Política</span><span class="sxs-lookup"><span data-stu-id="62399-129">-Policy</span></span>
<span data-ttu-id="62399-130">Especifica o nome da política de acesso armazenada que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="62399-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62399-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62399-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="62399-132">Especifica a duração do período de tempo de tempo para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="62399-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="62399-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="62399-133">-ShareName</span></span>
<span data-ttu-id="62399-134">Especifica o nome de compartilhamento de armazenamento para o qual este cmdlet remove uma política.</span><span class="sxs-lookup"><span data-stu-id="62399-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="62399-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62399-135">-Confirm</span></span>
<span data-ttu-id="62399-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62399-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62399-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62399-137">-WhatIf</span></span>
<span data-ttu-id="62399-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62399-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62399-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62399-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62399-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62399-140">CommonParameters</span></span>
<span data-ttu-id="62399-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62399-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62399-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62399-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62399-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="62399-143">INPUTS</span></span>

### <span data-ttu-id="62399-144">System.String</span><span class="sxs-lookup"><span data-stu-id="62399-144">System.String</span></span>

### <span data-ttu-id="62399-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="62399-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="62399-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="62399-146">OUTPUTS</span></span>

### <span data-ttu-id="62399-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62399-147">System.Boolean</span></span>

## <span data-ttu-id="62399-148">Notas</span><span class="sxs-lookup"><span data-stu-id="62399-148">NOTES</span></span>

## <span data-ttu-id="62399-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62399-149">RELATED LINKS</span></span>

[<span data-ttu-id="62399-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62399-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="62399-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62399-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="62399-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="62399-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="62399-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62399-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
