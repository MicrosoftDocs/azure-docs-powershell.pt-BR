---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954997"
---
# <span data-ttu-id="65d39-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="65d39-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="65d39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65d39-102">SYNOPSIS</span></span>
<span data-ttu-id="65d39-103">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="65d39-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="65d39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65d39-104">SYNTAX</span></span>

### <span data-ttu-id="65d39-105">ByString (padrão)</span><span class="sxs-lookup"><span data-stu-id="65d39-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="65d39-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="65d39-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65d39-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65d39-107">DESCRIPTION</span></span>
<span data-ttu-id="65d39-108">Cria uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="65d39-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="65d39-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65d39-109">EXAMPLES</span></span>

### <span data-ttu-id="65d39-110">Exemplo 1: criar uma instância do monitor SAP por cadeia de caracteres para HANA</span><span class="sxs-lookup"><span data-stu-id="65d39-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="65d39-111">Esse comando cria uma instância do monitor SAP por cadeia de caracteres para HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="65d39-112">Exemplo 2: criar uma instância do monitor SAP por um cofre de chaves para HANA</span><span class="sxs-lookup"><span data-stu-id="65d39-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="65d39-113">Esse comando cria uma instância do monitor SAP por um cofre de chaves para HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="65d39-114">OS</span><span class="sxs-lookup"><span data-stu-id="65d39-114">PARAMETERS</span></span>

### <span data-ttu-id="65d39-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65d39-115">-AsJob</span></span>
<span data-ttu-id="65d39-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="65d39-116">Run the command as a job</span></span>

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

### <span data-ttu-id="65d39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d39-117">-DefaultProfile</span></span>
<span data-ttu-id="65d39-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65d39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d39-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="65d39-119">-HanaDatabaseName</span></span>
<span data-ttu-id="65d39-120">O nome do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d39-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="65d39-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="65d39-122">A senha do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="65d39-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="65d39-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="65d39-124">ID do recurso do cofre de chaves que contém as credenciais do HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="65d39-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="65d39-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="65d39-126">Identificador de segredo para o segredo do cofre de chaves que contém as credenciais do HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="65d39-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="65d39-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="65d39-128">A porta SQL do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d39-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="65d39-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="65d39-130">O nome de usuário do banco de dados da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d39-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="65d39-131">-HanaHostname</span></span>
<span data-ttu-id="65d39-132">O nome do host da instância do SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="65d39-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="65d39-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="65d39-133">-Metadata</span></span>
<span data-ttu-id="65d39-134">Uma cadeia de caracteres JSON que contém metadados da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="65d39-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="65d39-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="65d39-135">-Name</span></span>
<span data-ttu-id="65d39-136">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="65d39-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="65d39-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="65d39-137">-NoWait</span></span>
<span data-ttu-id="65d39-138">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="65d39-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="65d39-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="65d39-139">-ProviderType</span></span>
<span data-ttu-id="65d39-140">O tipo de instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="65d39-140">The type of provider instance.</span></span>
<span data-ttu-id="65d39-141">Os valores com suporte são: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="65d39-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="65d39-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d39-142">-ResourceGroupName</span></span>
<span data-ttu-id="65d39-143">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65d39-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="65d39-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="65d39-144">-SapMonitorName</span></span>
<span data-ttu-id="65d39-145">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="65d39-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="65d39-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65d39-146">-SubscriptionId</span></span>
<span data-ttu-id="65d39-147">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="65d39-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="65d39-148">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="65d39-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="65d39-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65d39-149">-Confirm</span></span>
<span data-ttu-id="65d39-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d39-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d39-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d39-151">-WhatIf</span></span>
<span data-ttu-id="65d39-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65d39-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d39-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65d39-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d39-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d39-154">CommonParameters</span></span>
<span data-ttu-id="65d39-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d39-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d39-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65d39-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d39-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65d39-157">INPUTS</span></span>

## <span data-ttu-id="65d39-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65d39-158">OUTPUTS</span></span>

### <span data-ttu-id="65d39-159">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="65d39-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="65d39-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65d39-160">NOTES</span></span>

<span data-ttu-id="65d39-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="65d39-161">ALIASES</span></span>

## <span data-ttu-id="65d39-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65d39-162">RELATED LINKS</span></span>

