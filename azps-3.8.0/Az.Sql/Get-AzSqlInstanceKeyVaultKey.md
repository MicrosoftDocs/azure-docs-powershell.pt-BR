---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944262"
---
# <span data-ttu-id="a6ae8-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a6ae8-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="a6ae8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ae8-103">Obtém as chaves do cofre da chave de uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="a6ae8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6ae8-104">SYNTAX</span></span>

### <span data-ttu-id="a6ae8-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6ae8-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ae8-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6ae8-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ae8-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6ae8-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ae8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6ae8-108">DESCRIPTION</span></span>
<span data-ttu-id="a6ae8-109">O cmdlet Get-AzSqlInstanceKeyVaultKey Obtém informações sobre as chaves do cofre de chaves em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="a6ae8-110">Você pode exibir todas as chaves em uma instância gerenciada ou exibir uma chave específica fornecendo o KeyId.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="a6ae8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6ae8-111">EXAMPLES</span></span>

### <span data-ttu-id="a6ae8-112">Exemplo 1: obter todas as chaves do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a6ae8-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a6ae8-113">Esse comando obtém todas as chaves do cofre de chaves em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="a6ae8-114">Exemplo 2: obter uma chave específica do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a6ae8-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a6ae8-115">Este comando obtém a chave do cofre de chaves com a ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a6ae8-116">Exemplo 3: usando o objeto de instância</span><span class="sxs-lookup"><span data-stu-id="a6ae8-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a6ae8-117">Este comando obtém a chave do cofre de chaves com a ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a6ae8-118">Exemplo 4: usando a ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="a6ae8-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a6ae8-119">Este comando obtém a chave do cofre de chaves com a ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a6ae8-120">Exemplo 5: usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="a6ae8-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a6ae8-121">Este comando obtém a chave do cofre de chaves com a ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="a6ae8-122">OS</span><span class="sxs-lookup"><span data-stu-id="a6ae8-122">PARAMETERS</span></span>

### <span data-ttu-id="a6ae8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ae8-123">-DefaultProfile</span></span>
<span data-ttu-id="a6ae8-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="a6ae8-125">-Instance</span></span>
<span data-ttu-id="a6ae8-126">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="a6ae8-126">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a6ae8-127">-InstanceName</span></span>
<span data-ttu-id="a6ae8-128">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="a6ae8-128">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ae8-129">-InstanceResourceId</span></span>
<span data-ttu-id="a6ae8-130">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="a6ae8-130">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a6ae8-131">-KeyId</span></span>
<span data-ttu-id="a6ae8-132">ID da chave AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="a6ae8-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ae8-133">-ResourceGroupName</span></span>
<span data-ttu-id="a6ae8-134">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a6ae8-134">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae8-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6ae8-135">-Confirm</span></span>
<span data-ttu-id="a6ae8-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ae8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ae8-137">-WhatIf</span></span>
<span data-ttu-id="a6ae8-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ae8-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ae8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ae8-140">CommonParameters</span></span>
<span data-ttu-id="a6ae8-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ae8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ae8-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6ae8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ae8-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6ae8-143">INPUTS</span></span>

### <span data-ttu-id="a6ae8-144">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a6ae8-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="a6ae8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a6ae8-145">System.String</span></span>

## <span data-ttu-id="a6ae8-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6ae8-146">OUTPUTS</span></span>

### <span data-ttu-id="a6ae8-147">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="a6ae8-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="a6ae8-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6ae8-148">NOTES</span></span>

## <span data-ttu-id="a6ae8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6ae8-149">RELATED LINKS</span></span>
