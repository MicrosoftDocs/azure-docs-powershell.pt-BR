---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946050"
---
# <span data-ttu-id="9c4ea-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9c4ea-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="9c4ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4ea-103">Atualiza um trabalho do Agendador que tem uma ação de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="9c4ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c4ea-104">SYNTAX</span></span>

### <span data-ttu-id="9c4ea-105">Necessário</span><span class="sxs-lookup"><span data-stu-id="9c4ea-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c4ea-106">Recorrente</span><span class="sxs-lookup"><span data-stu-id="9c4ea-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c4ea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="9c4ea-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9c4ea-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9c4ea-110">O cmdlet **set-AzureSchedulerStorageQueueJob** atualiza um trabalho do Agendador que tem uma ação de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="9c4ea-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c4ea-111">EXAMPLES</span></span>

### <span data-ttu-id="9c4ea-112">Exemplo 1: atualizar uma mensagem de fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c4ea-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="9c4ea-113">Esse comando atualiza a mensagem da fila do trabalho de armazenamento chamado Job12.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="9c4ea-114">O comando especifica o nome da coleção de trabalhos e o local.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="9c4ea-115">Exemplo 2: habilitar um trabalho de fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9c4ea-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="9c4ea-116">Esse comando habilita o trabalho chamado Job16.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="9c4ea-117">O comando altera o estado do trabalho para habilitado especificando esse valor para o parâmetro *JobState* .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="9c4ea-118">OS</span><span class="sxs-lookup"><span data-stu-id="9c4ea-118">PARAMETERS</span></span>

### <span data-ttu-id="9c4ea-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9c4ea-119">-EndTime</span></span>
<span data-ttu-id="9c4ea-120">Especifica uma hora, como um objeto **DateTime** , para que o Agendador pare de iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="9c4ea-121">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="9c4ea-122">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="9c4ea-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="9c4ea-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="9c4ea-124">Especifica os cabeçalhos como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-124">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="9c4ea-125">-ErrorActionMethod</span></span>
<span data-ttu-id="9c4ea-126">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="9c4ea-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c4ea-127">Valid values are:</span></span> 

- <span data-ttu-id="9c4ea-128">Obter</span><span class="sxs-lookup"><span data-stu-id="9c4ea-128">GET</span></span>
- <span data-ttu-id="9c4ea-129">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="9c4ea-129">PUT</span></span>
- <span data-ttu-id="9c4ea-130">Postar</span><span class="sxs-lookup"><span data-stu-id="9c4ea-130">POST</span></span>
- <span data-ttu-id="9c4ea-131">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="9c4ea-131">HEAD</span></span>
- <span data-ttu-id="9c4ea-132">REMOVER</span><span class="sxs-lookup"><span data-stu-id="9c4ea-132">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="9c4ea-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="9c4ea-134">Especifica o corpo para ações de trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-134">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="9c4ea-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="9c4ea-136">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-136">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="9c4ea-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="9c4ea-138">Especifica o token de assinatura de acesso compartilhado (SAS) para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9c4ea-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="9c4ea-140">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-140">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9c4ea-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="9c4ea-142">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-142">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="9c4ea-143">-ErrorActionURI</span></span>
<span data-ttu-id="9c4ea-144">Especifica o URI da ação de trabalho de erro.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-144">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="9c4ea-145">-ExecutionCount</span></span>
<span data-ttu-id="9c4ea-146">Especifica o número de ocorrências de um trabalho que é executado.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="9c4ea-147">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="9c4ea-148">-Frequency</span><span class="sxs-lookup"><span data-stu-id="9c4ea-148">-Frequency</span></span>
<span data-ttu-id="9c4ea-149">Especifica a frequência máxima para este trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="9c4ea-150">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="9c4ea-150">-Interval</span></span>
<span data-ttu-id="9c4ea-151">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="9c4ea-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9c4ea-152">-JobCollectionName</span></span>
<span data-ttu-id="9c4ea-153">Especifica o nome da coleção que deve conter o trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-153">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="9c4ea-154">-JobName</span></span>
<span data-ttu-id="9c4ea-155">Especifica o nome do trabalho do Agendador a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-155">Specifies the name of the scheduler job to update.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="9c4ea-156">-JobState</span></span>
<span data-ttu-id="9c4ea-157">Especifica o estado do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-157">Specifies the state for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-158">-Local</span><span class="sxs-lookup"><span data-stu-id="9c4ea-158">-Location</span></span>
<span data-ttu-id="9c4ea-159">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="9c4ea-160">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c4ea-160">Valid values are:</span></span> 

- <span data-ttu-id="9c4ea-161">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="9c4ea-161">Anywhere Asia</span></span>
- <span data-ttu-id="9c4ea-162">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="9c4ea-162">Anywhere Europe</span></span>
- <span data-ttu-id="9c4ea-163">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-163">Anywhere US</span></span>
- <span data-ttu-id="9c4ea-164">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="9c4ea-164">East Asia</span></span>
- <span data-ttu-id="9c4ea-165">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-165">East US</span></span>
- <span data-ttu-id="9c4ea-166">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-166">North Central US</span></span>
- <span data-ttu-id="9c4ea-167">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="9c4ea-167">North Europe</span></span>
- <span data-ttu-id="9c4ea-168">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-168">South Central US</span></span>
- <span data-ttu-id="9c4ea-169">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="9c4ea-169">Southeast Asia</span></span>
- <span data-ttu-id="9c4ea-170">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="9c4ea-170">West Europe</span></span>
- <span data-ttu-id="9c4ea-171">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-171">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c4ea-172">-PassThru</span></span>
<span data-ttu-id="9c4ea-173">Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="9c4ea-174">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-174">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c4ea-175">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9c4ea-175">-Profile</span></span>
<span data-ttu-id="9c4ea-176">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c4ea-177">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="9c4ea-178">-SASToken</span></span>
<span data-ttu-id="9c4ea-179">Especifica o token SAS para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-179">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9c4ea-180">-StartTime</span></span>
<span data-ttu-id="9c4ea-181">Especifica uma hora, como um objeto **DateTime** , para que o trabalho seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="9c4ea-182">-StorageQueueAccount</span></span>
<span data-ttu-id="9c4ea-183">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-183">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="9c4ea-184">-StorageQueueMessage</span></span>
<span data-ttu-id="9c4ea-185">Especifica a mensagem da fila para o trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-185">Specifies the queue message for the Storage job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="9c4ea-186">-StorageQueueName</span></span>
<span data-ttu-id="9c4ea-187">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-187">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ea-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4ea-188">CommonParameters</span></span>
<span data-ttu-id="9c4ea-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4ea-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4ea-190">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4ea-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4ea-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c4ea-191">INPUTS</span></span>

## <span data-ttu-id="9c4ea-192">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c4ea-192">OUTPUTS</span></span>

## <span data-ttu-id="9c4ea-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c4ea-193">NOTES</span></span>

## <span data-ttu-id="9c4ea-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c4ea-194">RELATED LINKS</span></span>

[<span data-ttu-id="9c4ea-195">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="9c4ea-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


