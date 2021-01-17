---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429275"
---
# <span data-ttu-id="a43a2-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a43a2-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="a43a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a43a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a43a2-103">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a43a2-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a43a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a43a2-104">SYNTAX</span></span>

### <span data-ttu-id="a43a2-105">ByString (padrão)</span><span class="sxs-lookup"><span data-stu-id="a43a2-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a43a2-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="a43a2-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a43a2-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="a43a2-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a43a2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a43a2-108">DESCRIPTION</span></span>
<span data-ttu-id="a43a2-109">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a43a2-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="a43a2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a43a2-110">EXAMPLES</span></span>

### <span data-ttu-id="a43a2-111">Exemplo 1: criar uma instância do monitor SAP por cadeia de caracteres para HANA</span><span class="sxs-lookup"><span data-stu-id="a43a2-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-112">Esse comando cria uma instância do monitor SAP por cadeia de caracteres para HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="a43a2-113">Exemplo 2: criar uma instância do monitor SAP por um cofre de chaves para HANA</span><span class="sxs-lookup"><span data-stu-id="a43a2-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-114">Esse comando cria uma instância do monitor SAP por um cofre de chaves para HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="a43a2-115">Exemplo 3: criar uma instância do monitor SAP por dicionário para PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="a43a2-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-116">Esse comando cria uma instância do monitor SAP por dicionário para PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="a43a2-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="a43a2-117">Exemplo 4: criar uma instância do monitor SAP por dicionário para PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="a43a2-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-118">Esse comando cria uma instância do monitor SAP por dicionário para PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="a43a2-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="a43a2-119">Exemplo 5: criar uma instância do monitor SAP por dicionário para MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="a43a2-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-120">Esse comando cria uma instância do monitor SAP por dicionário para MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a43a2-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="a43a2-121">Exemplo 6: criar uma instância do monitor SAP por dicionário para SapHana</span><span class="sxs-lookup"><span data-stu-id="a43a2-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="a43a2-122">Esse comando cria uma instância do monitor SAP por dicionário para SapHana.</span><span class="sxs-lookup"><span data-stu-id="a43a2-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="a43a2-123">OS</span><span class="sxs-lookup"><span data-stu-id="a43a2-123">PARAMETERS</span></span>

### <span data-ttu-id="a43a2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a43a2-124">-AsJob</span></span>
<span data-ttu-id="a43a2-125">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a43a2-125">Run the command as a job</span></span>

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

### <span data-ttu-id="a43a2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43a2-126">-DefaultProfile</span></span>
<span data-ttu-id="a43a2-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a43a2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a43a2-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a43a2-128">-HanaDatabaseName</span></span>
<span data-ttu-id="a43a2-129">O nome do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-129">The database name of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="a43a2-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="a43a2-131">A senha do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-131">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="a43a2-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="a43a2-133">ID do recurso do cofre de chaves que contém as credenciais do HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="a43a2-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="a43a2-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="a43a2-135">Identificador de segredo para o segredo do cofre de chaves que contém as credenciais do HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="a43a2-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="a43a2-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="a43a2-137">A porta SQL do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-137">The SQL port of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="a43a2-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="a43a2-139">O nome de usuário do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-139">The username of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="a43a2-140">-HanaHostname</span></span>
<span data-ttu-id="a43a2-141">O nome do host da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-141">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="a43a2-142">-InstanceProperty</span></span>
<span data-ttu-id="a43a2-143">A propriedade de instância do HANA.</span><span class="sxs-lookup"><span data-stu-id="a43a2-143">The property of HANA instance.</span></span>

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

### <span data-ttu-id="a43a2-144">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a43a2-144">-Metadata</span></span>
<span data-ttu-id="a43a2-145">Uma cadeia de caracteres JSON que contém metadados da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="a43a2-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="a43a2-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="a43a2-146">-Name</span></span>
<span data-ttu-id="a43a2-147">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="a43a2-147">Name of the provider instance.</span></span>

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

### <span data-ttu-id="a43a2-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a43a2-148">-NoWait</span></span>
<span data-ttu-id="a43a2-149">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a43a2-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a43a2-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="a43a2-150">-ProviderType</span></span>
<span data-ttu-id="a43a2-151">O tipo de instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="a43a2-151">The type of provider instance.</span></span>
<span data-ttu-id="a43a2-152">Os valores com suporte são: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="a43a2-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="a43a2-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a43a2-153">-ResourceGroupName</span></span>
<span data-ttu-id="a43a2-154">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a43a2-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="a43a2-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="a43a2-155">-SapMonitorName</span></span>
<span data-ttu-id="a43a2-156">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="a43a2-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="a43a2-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a43a2-157">-SubscriptionId</span></span>
<span data-ttu-id="a43a2-158">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a43a2-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a43a2-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a43a2-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a43a2-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a43a2-160">-Confirm</span></span>
<span data-ttu-id="a43a2-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a43a2-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a43a2-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a43a2-162">-WhatIf</span></span>
<span data-ttu-id="a43a2-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a43a2-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a43a2-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a43a2-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a43a2-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43a2-165">CommonParameters</span></span>
<span data-ttu-id="a43a2-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43a2-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43a2-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a43a2-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43a2-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a43a2-168">INPUTS</span></span>

## <span data-ttu-id="a43a2-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a43a2-169">OUTPUTS</span></span>

### <span data-ttu-id="a43a2-170">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="a43a2-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="a43a2-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a43a2-171">NOTES</span></span>

<span data-ttu-id="a43a2-172">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a43a2-172">ALIASES</span></span>

## <span data-ttu-id="a43a2-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a43a2-173">RELATED LINKS</span></span>

