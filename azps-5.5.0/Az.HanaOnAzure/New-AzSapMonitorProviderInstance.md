---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113174"
---
# <span data-ttu-id="497e0-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="497e0-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="497e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="497e0-102">SYNOPSIS</span></span>
<span data-ttu-id="497e0-103">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="497e0-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="497e0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="497e0-104">SYNTAX</span></span>

### <span data-ttu-id="497e0-105">ByString (Padrão)</span><span class="sxs-lookup"><span data-stu-id="497e0-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="497e0-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="497e0-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="497e0-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="497e0-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="497e0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="497e0-108">DESCRIPTION</span></span>
<span data-ttu-id="497e0-109">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="497e0-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="497e0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="497e0-110">EXAMPLES</span></span>

### <span data-ttu-id="497e0-111">Exemplo 1: Criar uma instância do monitor SAP por cadeia de caracteres para HANA</span><span class="sxs-lookup"><span data-stu-id="497e0-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-112">Esse comando cria uma instância do monitor SAP por cadeia de caracteres para HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="497e0-113">Exemplo 2: Criar uma instância do monitor SAP por cofre de chave para HANA</span><span class="sxs-lookup"><span data-stu-id="497e0-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-114">Esse comando cria uma instância do monitor SAP por cofre de chave para HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="497e0-115">Exemplo 3: Criar uma instância do monitor SAP por dicionário para QueeusHaCluster</span><span class="sxs-lookup"><span data-stu-id="497e0-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-116">Esse comando cria uma instância do monitor SAP por dicionário para QuedaseusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="497e0-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="497e0-117">Exemplo 4: Criar uma instância do monitor SAP por dicionário para o MereusOS</span><span class="sxs-lookup"><span data-stu-id="497e0-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-118">Esse comando cria uma instância do monitor SAP por dicionário para QuedaseusOS.</span><span class="sxs-lookup"><span data-stu-id="497e0-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="497e0-119">Exemplo 5: Criar uma instância do monitor SAP por dicionário para MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="497e0-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-120">Esse comando cria uma instância do monitor SAP por dicionário para MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="497e0-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="497e0-121">Exemplo 6: Criar uma instância do monitor SAP por dicionário para SapHana</span><span class="sxs-lookup"><span data-stu-id="497e0-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="497e0-122">Esse comando cria uma instância do monitor SAP por dicionário para SapHana.</span><span class="sxs-lookup"><span data-stu-id="497e0-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="497e0-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="497e0-123">PARAMETERS</span></span>

### <span data-ttu-id="497e0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="497e0-124">-AsJob</span></span>
<span data-ttu-id="497e0-125">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="497e0-125">Run the command as a job</span></span>

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

### <span data-ttu-id="497e0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497e0-126">-DefaultProfile</span></span>
<span data-ttu-id="497e0-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="497e0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="497e0-128">-HanaDatabaseName</span></span>
<span data-ttu-id="497e0-129">O nome do banco de dados da instância SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="497e0-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="497e0-131">A senha do banco de dados da instância SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="497e0-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="497e0-133">ID do recurso do Cofre de Teclas que contém as credenciais HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-134">-HanaDatabasePasswordSecsecid</span><span class="sxs-lookup"><span data-stu-id="497e0-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="497e0-135">Identificador secreto do segredo do Cofre de Chaves que contém as credenciais HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="497e0-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="497e0-137">A porta SQL do banco de dados da instância SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="497e0-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="497e0-139">O nome de usuário do banco de dados da instância SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="497e0-140">-HanaHostname</span></span>
<span data-ttu-id="497e0-141">O nome do host da instância SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="497e0-142">-InstanceProperty</span></span>
<span data-ttu-id="497e0-143">A propriedade da instância HANA.</span><span class="sxs-lookup"><span data-stu-id="497e0-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="497e0-144">-Metadata</span></span>
<span data-ttu-id="497e0-145">Uma cadeia de caracteres JSON que contém metadados da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="497e0-145">A JSON string containing metadata of the provider instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="497e0-146">-Name</span></span>
<span data-ttu-id="497e0-147">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="497e0-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="497e0-148">-NoWait</span></span>
<span data-ttu-id="497e0-149">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="497e0-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="497e0-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="497e0-150">-ProviderType</span></span>
<span data-ttu-id="497e0-151">O tipo de instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="497e0-151">The type of provider instance.</span></span>
<span data-ttu-id="497e0-152">Os valores com suporte são: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="497e0-152">Supported values are: "SapHana".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497e0-153">-ResourceGroupName</span></span>
<span data-ttu-id="497e0-154">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="497e0-154">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="497e0-155">-SapMonitorName</span></span>
<span data-ttu-id="497e0-156">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="497e0-156">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="497e0-157">-SubscriptionId</span></span>
<span data-ttu-id="497e0-158">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="497e0-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="497e0-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="497e0-159">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-160">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="497e0-160">-Confirm</span></span>
<span data-ttu-id="497e0-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="497e0-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497e0-162">-WhatIf</span></span>
<span data-ttu-id="497e0-163">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="497e0-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497e0-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="497e0-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497e0-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497e0-165">CommonParameters</span></span>
<span data-ttu-id="497e0-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497e0-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497e0-167">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="497e0-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497e0-168">Entradas</span><span class="sxs-lookup"><span data-stu-id="497e0-168">INPUTS</span></span>

## <span data-ttu-id="497e0-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="497e0-169">OUTPUTS</span></span>

### <span data-ttu-id="497e0-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="497e0-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="497e0-171">Notas</span><span class="sxs-lookup"><span data-stu-id="497e0-171">NOTES</span></span>

<span data-ttu-id="497e0-172">Aliases</span><span class="sxs-lookup"><span data-stu-id="497e0-172">ALIASES</span></span>

## <span data-ttu-id="497e0-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="497e0-173">RELATED LINKS</span></span>

