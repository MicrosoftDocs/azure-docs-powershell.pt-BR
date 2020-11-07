---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945799"
---
# <span data-ttu-id="30be5-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="30be5-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="30be5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30be5-102">SYNOPSIS</span></span>
<span data-ttu-id="30be5-103">Atualiza um trabalho do Agendador com uma ação HTTP.</span><span class="sxs-lookup"><span data-stu-id="30be5-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="30be5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30be5-104">SYNTAX</span></span>

### <span data-ttu-id="30be5-105">Necessário</span><span class="sxs-lookup"><span data-stu-id="30be5-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="30be5-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="30be5-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30be5-107">Recorrente</span><span class="sxs-lookup"><span data-stu-id="30be5-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30be5-108">Autenticação</span><span class="sxs-lookup"><span data-stu-id="30be5-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30be5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30be5-109">DESCRIPTION</span></span>
<span data-ttu-id="30be5-110">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30be5-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30be5-111">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="30be5-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="30be5-112">O cmdlet **set-AzureSchedulerHttpJob** atualiza um trabalho do Agendador com uma ação http.</span><span class="sxs-lookup"><span data-stu-id="30be5-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="30be5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30be5-113">EXAMPLES</span></span>

### <span data-ttu-id="30be5-114">Exemplo 1: alterar o estado de um trabalho para desabilitado</span><span class="sxs-lookup"><span data-stu-id="30be5-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="30be5-115">Esse comando altera o estado do trabalho denominado Job01 para desabilitado.</span><span class="sxs-lookup"><span data-stu-id="30be5-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="30be5-116">Esse trabalho faz parte da coleção de trabalhos chamada JobColleciton01 para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="30be5-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="30be5-117">Exemplo 2: atualizar o URI de um trabalho</span><span class="sxs-lookup"><span data-stu-id="30be5-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="30be5-118">Esse comando atualiza o URI do trabalho chamado Job01 http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="30be5-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="30be5-119">OS</span><span class="sxs-lookup"><span data-stu-id="30be5-119">PARAMETERS</span></span>

### <span data-ttu-id="30be5-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="30be5-120">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="30be5-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="30be5-121">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="30be5-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="30be5-122">-EndTime</span></span>
<span data-ttu-id="30be5-123">Especifica uma hora, como um objeto **DateTime** , para que o Agendador pare de iniciar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="30be5-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="30be5-124">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="30be5-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="30be5-125">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="30be5-125">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="30be5-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="30be5-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="30be5-127">Especifica os cabeçalhos como uma Hashtable.</span><span class="sxs-lookup"><span data-stu-id="30be5-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="30be5-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="30be5-128">-ErrorActionMethod</span></span>
<span data-ttu-id="30be5-129">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="30be5-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="30be5-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="30be5-130">Valid values are:</span></span> 

- <span data-ttu-id="30be5-131">Obter</span><span class="sxs-lookup"><span data-stu-id="30be5-131">GET</span></span>
- <span data-ttu-id="30be5-132">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="30be5-132">PUT</span></span>
- <span data-ttu-id="30be5-133">Postar</span><span class="sxs-lookup"><span data-stu-id="30be5-133">POST</span></span>
- <span data-ttu-id="30be5-134">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="30be5-134">HEAD</span></span>
- <span data-ttu-id="30be5-135">REMOVER</span><span class="sxs-lookup"><span data-stu-id="30be5-135">DELETE</span></span>

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

### <span data-ttu-id="30be5-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="30be5-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="30be5-137">Especifica o corpo para ações de trabalho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30be5-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="30be5-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="30be5-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="30be5-139">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="30be5-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="30be5-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="30be5-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="30be5-141">Especifica o token de assinatura de acesso compartilhado (SAS) para a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30be5-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="30be5-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30be5-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="30be5-143">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30be5-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="30be5-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="30be5-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="30be5-145">Especifica o nome da fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30be5-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="30be5-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="30be5-146">-ErrorActionURI</span></span>
<span data-ttu-id="30be5-147">Especifica o URI da ação de trabalho de erro.</span><span class="sxs-lookup"><span data-stu-id="30be5-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="30be5-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="30be5-148">-ExecutionCount</span></span>
<span data-ttu-id="30be5-149">Especifica o número de ocorrências de um trabalho que é executado.</span><span class="sxs-lookup"><span data-stu-id="30be5-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="30be5-150">Por padrão, um trabalho se repete indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="30be5-150">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="30be5-151">-Frequency</span><span class="sxs-lookup"><span data-stu-id="30be5-151">-Frequency</span></span>
<span data-ttu-id="30be5-152">Especifica a frequência máxima para este trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="30be5-152">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="30be5-153">-Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="30be5-153">-Headers</span></span>
<span data-ttu-id="30be5-154">Especifica os cabeçalhos como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="30be5-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="30be5-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="30be5-155">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="30be5-156">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="30be5-156">-Interval</span></span>
<span data-ttu-id="30be5-157">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="30be5-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="30be5-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="30be5-158">-JobCollectionName</span></span>
<span data-ttu-id="30be5-159">Especifica o nome da coleção que contém o trabalho do Agendador a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="30be5-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="30be5-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="30be5-160">-JobName</span></span>
<span data-ttu-id="30be5-161">Especifica o nome do trabalho do Agendador a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="30be5-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="30be5-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="30be5-162">-JobState</span></span>
<span data-ttu-id="30be5-163">Especifica o estado do trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="30be5-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="30be5-164">-Local</span><span class="sxs-lookup"><span data-stu-id="30be5-164">-Location</span></span>
<span data-ttu-id="30be5-165">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="30be5-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="30be5-166">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="30be5-166">Valid values are:</span></span> 

- <span data-ttu-id="30be5-167">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="30be5-167">Anywhere Asia</span></span>
- <span data-ttu-id="30be5-168">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="30be5-168">Anywhere Europe</span></span>
- <span data-ttu-id="30be5-169">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="30be5-169">Anywhere US</span></span>
- <span data-ttu-id="30be5-170">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="30be5-170">East Asia</span></span>
- <span data-ttu-id="30be5-171">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="30be5-171">East US</span></span>
- <span data-ttu-id="30be5-172">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="30be5-172">North Central US</span></span>
- <span data-ttu-id="30be5-173">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="30be5-173">North Europe</span></span>
- <span data-ttu-id="30be5-174">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="30be5-174">South Central US</span></span>
- <span data-ttu-id="30be5-175">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="30be5-175">Southeast Asia</span></span>
- <span data-ttu-id="30be5-176">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="30be5-176">West Europe</span></span>
- <span data-ttu-id="30be5-177">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="30be5-177">West US</span></span>

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

### <span data-ttu-id="30be5-178">-Método</span><span class="sxs-lookup"><span data-stu-id="30be5-178">-Method</span></span>
<span data-ttu-id="30be5-179">Especifica o método para tipos de ação HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="30be5-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="30be5-180">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="30be5-180">Valid values are:</span></span> 

- <span data-ttu-id="30be5-181">Obter</span><span class="sxs-lookup"><span data-stu-id="30be5-181">GET</span></span>
- <span data-ttu-id="30be5-182">SUSPENDE</span><span class="sxs-lookup"><span data-stu-id="30be5-182">PUT</span></span>
- <span data-ttu-id="30be5-183">Postar</span><span class="sxs-lookup"><span data-stu-id="30be5-183">POST</span></span>
- <span data-ttu-id="30be5-184">CUSTOS</span><span class="sxs-lookup"><span data-stu-id="30be5-184">HEAD</span></span>
- <span data-ttu-id="30be5-185">REMOVER</span><span class="sxs-lookup"><span data-stu-id="30be5-185">DELETE</span></span>

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

### <span data-ttu-id="30be5-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30be5-186">-PassThru</span></span>
<span data-ttu-id="30be5-187">Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.</span><span class="sxs-lookup"><span data-stu-id="30be5-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="30be5-188">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="30be5-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30be5-189">-Perfil</span><span class="sxs-lookup"><span data-stu-id="30be5-189">-Profile</span></span>
<span data-ttu-id="30be5-190">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="30be5-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30be5-191">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="30be5-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30be5-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="30be5-192">-RequestBody</span></span>
<span data-ttu-id="30be5-193">Especifica o corpo para colocar e postar ações de trabalho.</span><span class="sxs-lookup"><span data-stu-id="30be5-193">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="30be5-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="30be5-194">-StartTime</span></span>
<span data-ttu-id="30be5-195">Especifica uma hora, como um objeto **DateTime** , para que o trabalho seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="30be5-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="30be5-196">-URI</span><span class="sxs-lookup"><span data-stu-id="30be5-196">-URI</span></span>
<span data-ttu-id="30be5-197">Especifica um URI para uma ação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="30be5-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="30be5-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30be5-198">CommonParameters</span></span>
<span data-ttu-id="30be5-199">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30be5-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30be5-200">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30be5-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30be5-201">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30be5-201">INPUTS</span></span>

## <span data-ttu-id="30be5-202">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30be5-202">OUTPUTS</span></span>

## <span data-ttu-id="30be5-203">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30be5-203">NOTES</span></span>

## <span data-ttu-id="30be5-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30be5-204">RELATED LINKS</span></span>

[<span data-ttu-id="30be5-205">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="30be5-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


