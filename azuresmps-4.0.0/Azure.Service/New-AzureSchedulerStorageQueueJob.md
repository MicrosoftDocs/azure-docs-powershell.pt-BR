---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945902"
---
# <span data-ttu-id="a2ba1-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a2ba1-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="a2ba1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ba1-103">Cria um trabalho do Agendador com uma ação de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="a2ba1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2ba1-104">SYNTAX</span></span>

### <span data-ttu-id="a2ba1-105">Necessário</span><span class="sxs-lookup"><span data-stu-id="a2ba1-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a2ba1-106">Recorrente</span><span class="sxs-lookup"><span data-stu-id="a2ba1-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2ba1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2ba1-107">DESCRIPTION</span></span>
<span data-ttu-id="a2ba1-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a2ba1-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a2ba1-110">O cmdlet **New-AzureSchedulerStorageQueueJob** cria um trabalho do Agendador com uma ação de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="a2ba1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="a2ba1-112">Exemplo 1: criar um trabalho de armazenamento que seja executado uma vez</span><span class="sxs-lookup"><span data-stu-id="a2ba1-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="a2ba1-113">Esse comando cria um trabalho de armazenamento do Agendador como parte da coleção chamada JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="a2ba1-114">O comando especifica a conta de armazenamento, o nome da fila e o token SAS.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="a2ba1-115">O trabalho é executado uma vez, imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="a2ba1-116">Exemplo 2: criar um trabalho de armazenamento que executa um número especificado de vezes</span><span class="sxs-lookup"><span data-stu-id="a2ba1-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="a2ba1-117">Esse comando cria um trabalho de armazenamento do Agendador como parte da coleção chamada JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="a2ba1-118">O comando especifica a conta de armazenamento, o nome da fila e o token SAS.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="a2ba1-119">O trabalho é executado 20 vezes no total, duas vezes a cada hora.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="a2ba1-120">OS</span><span class="sxs-lookup"><span data-stu-id="a2ba1-120">PARAMETERS</span></span>

### <span data-ttu-id="a2ba1-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a2ba1-121">-EndTime</span></span>
<span data-ttu-id="a2ba1-122">Especifica uma hora, como um objeto **DateTime** , para que o Agendador pare de iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="a2ba1-123">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="a2ba1-124">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="a2ba1-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="a2ba1-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="a2ba1-126">Especifica os cabeçalhos como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="a2ba1-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="a2ba1-127">-ErrorActionMethod</span></span>
<span data-ttu-id="a2ba1-128">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="a2ba1-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a2ba1-129">Valid values are:</span></span> 

- <span data-ttu-id="a2ba1-130">Obter</span><span class="sxs-lookup"><span data-stu-id="a2ba1-130">GET</span></span>
- <span data-ttu-id="a2ba1-131">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="a2ba1-131">PUT</span></span>
- <span data-ttu-id="a2ba1-132">Postar</span><span class="sxs-lookup"><span data-stu-id="a2ba1-132">POST</span></span>
- <span data-ttu-id="a2ba1-133">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="a2ba1-133">HEAD</span></span>
- <span data-ttu-id="a2ba1-134">REMOVER</span><span class="sxs-lookup"><span data-stu-id="a2ba1-134">DELETE</span></span>

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

### <span data-ttu-id="a2ba1-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="a2ba1-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="a2ba1-136">Especifica o corpo para ações de trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-136">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="a2ba1-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="a2ba1-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="a2ba1-138">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-138">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="a2ba1-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="a2ba1-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="a2ba1-140">Especifica o token de assinatura de acesso compartilhado (SAS) para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="a2ba1-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2ba1-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="a2ba1-142">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-142">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="a2ba1-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a2ba1-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="a2ba1-144">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-144">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="a2ba1-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="a2ba1-145">-ErrorActionURI</span></span>
<span data-ttu-id="a2ba1-146">Especifica o URI da ação de trabalho de erro.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-146">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="a2ba1-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a2ba1-147">-ExecutionCount</span></span>
<span data-ttu-id="a2ba1-148">Especifica o número de ocorrências de um trabalho que é executado.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="a2ba1-149">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a2ba1-150">-Frequency</span><span class="sxs-lookup"><span data-stu-id="a2ba1-150">-Frequency</span></span>
<span data-ttu-id="a2ba1-151">Especifica a frequência máxima para este trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="a2ba1-152">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="a2ba1-152">-Interval</span></span>
<span data-ttu-id="a2ba1-153">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="a2ba1-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a2ba1-154">-JobCollectionName</span></span>
<span data-ttu-id="a2ba1-155">Especifica o nome da coleção que deve conter o trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-155">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="a2ba1-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="a2ba1-156">-JobName</span></span>
<span data-ttu-id="a2ba1-157">Especifica o nome do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-157">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="a2ba1-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="a2ba1-158">-JobState</span></span>
<span data-ttu-id="a2ba1-159">Especifica o estado do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="a2ba1-160">-Local</span><span class="sxs-lookup"><span data-stu-id="a2ba1-160">-Location</span></span>
<span data-ttu-id="a2ba1-161">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="a2ba1-162">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a2ba1-162">Valid values are:</span></span> 

- <span data-ttu-id="a2ba1-163">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="a2ba1-163">Anywhere Asia</span></span>
- <span data-ttu-id="a2ba1-164">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="a2ba1-164">Anywhere Europe</span></span>
- <span data-ttu-id="a2ba1-165">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-165">Anywhere US</span></span>
- <span data-ttu-id="a2ba1-166">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="a2ba1-166">East Asia</span></span>
- <span data-ttu-id="a2ba1-167">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-167">East US</span></span>
- <span data-ttu-id="a2ba1-168">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-168">North Central US</span></span>
- <span data-ttu-id="a2ba1-169">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="a2ba1-169">North Europe</span></span>
- <span data-ttu-id="a2ba1-170">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-170">South Central US</span></span>
- <span data-ttu-id="a2ba1-171">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="a2ba1-171">Southeast Asia</span></span>
- <span data-ttu-id="a2ba1-172">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="a2ba1-172">West Europe</span></span>
- <span data-ttu-id="a2ba1-173">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-173">West US</span></span>

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

### <span data-ttu-id="a2ba1-174">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a2ba1-174">-Profile</span></span>
<span data-ttu-id="a2ba1-175">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2ba1-176">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2ba1-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="a2ba1-177">-SASToken</span></span>
<span data-ttu-id="a2ba1-178">Especifica o token SAS para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-178">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="a2ba1-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a2ba1-179">-StartTime</span></span>
<span data-ttu-id="a2ba1-180">Especifica uma hora, como um objeto **DateTime** , para que o trabalho seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="a2ba1-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="a2ba1-181">-StorageQueueAccount</span></span>
<span data-ttu-id="a2ba1-182">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-182">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="a2ba1-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="a2ba1-183">-StorageQueueMessage</span></span>
<span data-ttu-id="a2ba1-184">Especifica a mensagem da fila para o trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="a2ba1-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="a2ba1-185">-StorageQueueName</span></span>
<span data-ttu-id="a2ba1-186">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-186">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="a2ba1-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ba1-187">CommonParameters</span></span>
<span data-ttu-id="a2ba1-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ba1-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ba1-189">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ba1-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ba1-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2ba1-190">INPUTS</span></span>

## <span data-ttu-id="a2ba1-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2ba1-191">OUTPUTS</span></span>

## <span data-ttu-id="a2ba1-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2ba1-192">NOTES</span></span>

## <span data-ttu-id="a2ba1-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2ba1-193">RELATED LINKS</span></span>

[<span data-ttu-id="a2ba1-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a2ba1-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


