---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: c0db10c24f019a9f91efd4ad9ec6805ffc3b0208
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785277"
---
# <span data-ttu-id="115c4-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="115c4-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="115c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="115c4-102">SYNOPSIS</span></span>
<span data-ttu-id="115c4-103">Interrompe uma operação de cópia para o arquivo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="115c4-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="115c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="115c4-104">SYNTAX</span></span>

### <span data-ttu-id="115c4-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="115c4-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="115c4-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="115c4-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="115c4-107">DESCRIPTION</span></span>
<span data-ttu-id="115c4-108">O cmdlet **Stop-AzureStorageFileCopy** interrompe a cópia de um arquivo para um arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="115c4-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="115c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="115c4-109">EXAMPLES</span></span>

### <span data-ttu-id="115c4-110">Exemplo 1: parar uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="115c4-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="115c4-111">Esse comando para de copiar um arquivo com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="115c4-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="115c4-112">OS</span><span class="sxs-lookup"><span data-stu-id="115c4-112">PARAMETERS</span></span>

### <span data-ttu-id="115c4-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="115c4-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="115c4-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="115c4-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="115c4-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="115c4-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="115c4-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="115c4-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="115c4-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="115c4-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="115c4-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="115c4-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="115c4-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="115c4-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="115c4-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="115c4-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="115c4-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="115c4-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="115c4-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="115c4-122">The default value is 10.</span></span>

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

### <span data-ttu-id="115c4-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="115c4-123">-Context</span></span>
<span data-ttu-id="115c4-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="115c4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="115c4-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="115c4-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="115c4-126">-Copyid</span><span class="sxs-lookup"><span data-stu-id="115c4-126">-CopyId</span></span>
<span data-ttu-id="115c4-127">Especifica a ID da operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="115c4-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115c4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115c4-128">-DefaultProfile</span></span>
<span data-ttu-id="115c4-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="115c4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="115c4-130">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="115c4-130">-File</span></span>
<span data-ttu-id="115c4-131">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="115c4-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="115c4-132">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="115c4-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="115c4-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="115c4-133">-FilePath</span></span>
<span data-ttu-id="115c4-134">Especifica o caminho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="115c4-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115c4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="115c4-135">-Force</span></span>
<span data-ttu-id="115c4-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="115c4-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="115c4-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="115c4-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="115c4-138">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="115c4-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="115c4-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="115c4-139">-ShareName</span></span>
<span data-ttu-id="115c4-140">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="115c4-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115c4-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="115c4-141">-Confirm</span></span>
<span data-ttu-id="115c4-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="115c4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="115c4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115c4-143">-WhatIf</span></span>
<span data-ttu-id="115c4-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="115c4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115c4-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="115c4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="115c4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115c4-146">CommonParameters</span></span>
<span data-ttu-id="115c4-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115c4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115c4-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="115c4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115c4-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="115c4-149">INPUTS</span></span>

### <span data-ttu-id="115c4-150">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="115c4-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="115c4-151">Parâmetros: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="115c4-151">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="115c4-152">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="115c4-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="115c4-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="115c4-153">OUTPUTS</span></span>

### <span data-ttu-id="115c4-154">System. void</span><span class="sxs-lookup"><span data-stu-id="115c4-154">System.Void</span></span>

## <span data-ttu-id="115c4-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="115c4-155">NOTES</span></span>

## <span data-ttu-id="115c4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="115c4-156">RELATED LINKS</span></span>

[<span data-ttu-id="115c4-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="115c4-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="115c4-158">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="115c4-158">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="115c4-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="115c4-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="115c4-160">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="115c4-160">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
