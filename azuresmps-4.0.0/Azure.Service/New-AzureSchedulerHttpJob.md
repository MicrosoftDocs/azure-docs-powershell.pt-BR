---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945904"
---
# <span data-ttu-id="f387f-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f387f-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="f387f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f387f-102">SYNOPSIS</span></span>
<span data-ttu-id="f387f-103">Cria um trabalho do Agendador com uma ação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f387f-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="f387f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f387f-104">SYNTAX</span></span>

### <span data-ttu-id="f387f-105">Necessário</span><span class="sxs-lookup"><span data-stu-id="f387f-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f387f-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="f387f-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f387f-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="f387f-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f387f-108">Autenticação</span><span class="sxs-lookup"><span data-stu-id="f387f-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f387f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f387f-109">DESCRIPTION</span></span>
<span data-ttu-id="f387f-110">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f387f-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f387f-111">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f387f-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f387f-112">O cmdlet **New-AzureSchedulerHttpJob** cria um trabalho do Agendador com uma ação http.</span><span class="sxs-lookup"><span data-stu-id="f387f-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="f387f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f387f-113">EXAMPLES</span></span>

### <span data-ttu-id="f387f-114">Exemplo 1: criar um trabalho HTTP</span><span class="sxs-lookup"><span data-stu-id="f387f-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="f387f-115">Esse comando cria um trabalho de Agendador HTTP na coleção de trabalhos chamado JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="f387f-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="f387f-116">O comando especifica um URI e especifica GET como o método.</span><span class="sxs-lookup"><span data-stu-id="f387f-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="f387f-117">Exemplo 2: criar um trabalho HTTP para uma contagem específica de execuções</span><span class="sxs-lookup"><span data-stu-id="f387f-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="f387f-118">Esse comando cria o trabalho do Agendador http na coleção de trabalhos chamada JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="f387f-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="f387f-119">O comando especifica um URI e especifica GET como o método.</span><span class="sxs-lookup"><span data-stu-id="f387f-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="f387f-120">Esse comando faz com que o trabalho seja executado 20 vezes.</span><span class="sxs-lookup"><span data-stu-id="f387f-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="f387f-121">OS</span><span class="sxs-lookup"><span data-stu-id="f387f-121">PARAMETERS</span></span>

### <span data-ttu-id="f387f-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f387f-122">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="f387f-123">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f387f-124">-EndTime</span></span>
<span data-ttu-id="f387f-125">Especifica uma hora, como um objeto **DateTime** , para que o Agendador pare de iniciar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="f387f-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="f387f-126">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="f387f-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f387f-127">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f387f-127">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="f387f-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="f387f-129">Especifica os cabeçalhos como uma Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f387f-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="f387f-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="f387f-130">-ErrorActionMethod</span></span>
<span data-ttu-id="f387f-131">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f387f-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="f387f-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f387f-132">Valid values are:</span></span> 

- <span data-ttu-id="f387f-133">Obter</span><span class="sxs-lookup"><span data-stu-id="f387f-133">GET</span></span>
- <span data-ttu-id="f387f-134">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="f387f-134">PUT</span></span>
- <span data-ttu-id="f387f-135">Postar</span><span class="sxs-lookup"><span data-stu-id="f387f-135">POST</span></span>
- <span data-ttu-id="f387f-136">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="f387f-136">HEAD</span></span>
- <span data-ttu-id="f387f-137">REMOVER</span><span class="sxs-lookup"><span data-stu-id="f387f-137">DELETE</span></span>

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

### <span data-ttu-id="f387f-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="f387f-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="f387f-139">Especifica o corpo para ações de trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f387f-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="f387f-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="f387f-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="f387f-141">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f387f-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="f387f-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="f387f-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="f387f-143">Especifica o token de assinatura de acesso compartilhado (SAS) para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f387f-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="f387f-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f387f-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="f387f-145">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f387f-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="f387f-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="f387f-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="f387f-147">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f387f-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="f387f-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="f387f-148">-ErrorActionURI</span></span>
<span data-ttu-id="f387f-149">Especifica o URI da ação de trabalho de erro.</span><span class="sxs-lookup"><span data-stu-id="f387f-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="f387f-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="f387f-150">-ExecutionCount</span></span>
<span data-ttu-id="f387f-151">Especifica o número de ocorrências de um trabalho que é executado.</span><span class="sxs-lookup"><span data-stu-id="f387f-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="f387f-152">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="f387f-152">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-153">-Frequency</span><span class="sxs-lookup"><span data-stu-id="f387f-153">-Frequency</span></span>
<span data-ttu-id="f387f-154">Especifica a frequência máxima para este trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="f387f-154">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-155">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="f387f-155">-Headers</span></span>
<span data-ttu-id="f387f-156">Especifica os cabeçalhos como uma Hashtable.</span><span class="sxs-lookup"><span data-stu-id="f387f-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="f387f-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f387f-157">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-158">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="f387f-158">-Interval</span></span>
<span data-ttu-id="f387f-159">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="f387f-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f387f-160">-JobCollectionName</span></span>
<span data-ttu-id="f387f-161">Especifica o nome da coleção que deve conter o trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="f387f-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="f387f-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="f387f-162">-JobName</span></span>
<span data-ttu-id="f387f-163">Especifica o nome do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="f387f-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="f387f-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="f387f-164">-JobState</span></span>
<span data-ttu-id="f387f-165">Especifica o estado do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="f387f-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="f387f-166">-Local</span><span class="sxs-lookup"><span data-stu-id="f387f-166">-Location</span></span>
<span data-ttu-id="f387f-167">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="f387f-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="f387f-168">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f387f-168">Valid values are:</span></span> 

- <span data-ttu-id="f387f-169">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="f387f-169">Anywhere Asia</span></span>
- <span data-ttu-id="f387f-170">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="f387f-170">Anywhere Europe</span></span>
- <span data-ttu-id="f387f-171">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="f387f-171">Anywhere US</span></span>
- <span data-ttu-id="f387f-172">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="f387f-172">East Asia</span></span>
- <span data-ttu-id="f387f-173">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f387f-173">East US</span></span>
- <span data-ttu-id="f387f-174">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="f387f-174">North Central US</span></span>
- <span data-ttu-id="f387f-175">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="f387f-175">North Europe</span></span>
- <span data-ttu-id="f387f-176">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="f387f-176">South Central US</span></span>
- <span data-ttu-id="f387f-177">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="f387f-177">Southeast Asia</span></span>
- <span data-ttu-id="f387f-178">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="f387f-178">West Europe</span></span>
- <span data-ttu-id="f387f-179">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f387f-179">West US</span></span>

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

### <span data-ttu-id="f387f-180">-Método</span><span class="sxs-lookup"><span data-stu-id="f387f-180">-Method</span></span>
<span data-ttu-id="f387f-181">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f387f-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="f387f-182">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f387f-182">Valid values are:</span></span> 

- <span data-ttu-id="f387f-183">Obter</span><span class="sxs-lookup"><span data-stu-id="f387f-183">GET</span></span>
- <span data-ttu-id="f387f-184">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="f387f-184">PUT</span></span>
- <span data-ttu-id="f387f-185">Postar</span><span class="sxs-lookup"><span data-stu-id="f387f-185">POST</span></span>
- <span data-ttu-id="f387f-186">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="f387f-186">HEAD</span></span>
- <span data-ttu-id="f387f-187">REMOVER</span><span class="sxs-lookup"><span data-stu-id="f387f-187">DELETE</span></span>

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

### <span data-ttu-id="f387f-188">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f387f-188">-Profile</span></span>
<span data-ttu-id="f387f-189">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f387f-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f387f-190">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f387f-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f387f-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="f387f-191">-RequestBody</span></span>
<span data-ttu-id="f387f-192">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f387f-192">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f387f-193">-StartTime</span></span>
<span data-ttu-id="f387f-194">Especifica uma hora, como um objeto **DateTime** , para que o trabalho seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="f387f-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="f387f-195">-URI</span><span class="sxs-lookup"><span data-stu-id="f387f-195">-URI</span></span>
<span data-ttu-id="f387f-196">Especifica um URI para uma ação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f387f-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f387f-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f387f-197">CommonParameters</span></span>
<span data-ttu-id="f387f-198">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f387f-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f387f-199">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f387f-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f387f-200">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f387f-200">INPUTS</span></span>

## <span data-ttu-id="f387f-201">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f387f-201">OUTPUTS</span></span>

## <span data-ttu-id="f387f-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f387f-202">NOTES</span></span>

## <span data-ttu-id="f387f-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f387f-203">RELATED LINKS</span></span>

[<span data-ttu-id="f387f-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f387f-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


