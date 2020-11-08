---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115828"
---
# <span data-ttu-id="f934e-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f934e-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="f934e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f934e-102">SYNOPSIS</span></span>
<span data-ttu-id="f934e-103">Obtém o protetor de criptografia de dados transparente (TDE) para uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="f934e-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="f934e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f934e-104">SYNTAX</span></span>

### <span data-ttu-id="f934e-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f934e-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f934e-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f934e-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f934e-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f934e-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f934e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f934e-108">DESCRIPTION</span></span>
<span data-ttu-id="f934e-109">O cmdlet Get-AzSqlInstanceTransparentDataEncryptionProtector Obtém o protetor TDE para a instância gerenciada SQL especificada.</span><span class="sxs-lookup"><span data-stu-id="f934e-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="f934e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f934e-110">EXAMPLES</span></span>

### <span data-ttu-id="f934e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f934e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="f934e-112">Esse comando obtém o protetor TDE para a instância gerenciada chamada ContosoManagedInstanceName no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f934e-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f934e-113">Exemplo 2: usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="f934e-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="f934e-114">Esse comando obtém o protetor TDE para a instância gerenciada chamada ContosoManagedInstanceName no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f934e-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f934e-115">Exemplo 3: usando a ID do recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="f934e-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="f934e-116">Esse comando obtém o protetor TDE para a instância gerenciada chamada ContosoManagedInstanceName no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f934e-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f934e-117">Exemplo 4: usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="f934e-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="f934e-118">Esse comando obtém o protetor TDE para a instância gerenciada chamada ContosoManagedInstanceName no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f934e-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f934e-119">OS</span><span class="sxs-lookup"><span data-stu-id="f934e-119">PARAMETERS</span></span>

### <span data-ttu-id="f934e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f934e-120">-DefaultProfile</span></span>
<span data-ttu-id="f934e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f934e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f934e-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="f934e-122">-Instance</span></span>
<span data-ttu-id="f934e-123">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="f934e-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f934e-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f934e-124">-InstanceName</span></span>
<span data-ttu-id="f934e-125">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="f934e-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f934e-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="f934e-126">-InstanceResourceId</span></span>
<span data-ttu-id="f934e-127">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="f934e-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f934e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f934e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f934e-129">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f934e-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f934e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f934e-130">-Confirm</span></span>
<span data-ttu-id="f934e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f934e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f934e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f934e-132">-WhatIf</span></span>
<span data-ttu-id="f934e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f934e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f934e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f934e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f934e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f934e-135">CommonParameters</span></span>
<span data-ttu-id="f934e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f934e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f934e-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f934e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f934e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f934e-138">INPUTS</span></span>

### <span data-ttu-id="f934e-139">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f934e-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="f934e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f934e-140">System.String</span></span>

## <span data-ttu-id="f934e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f934e-141">OUTPUTS</span></span>

### <span data-ttu-id="f934e-142">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="f934e-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="f934e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f934e-143">NOTES</span></span>

## <span data-ttu-id="f934e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f934e-144">RELATED LINKS</span></span>
