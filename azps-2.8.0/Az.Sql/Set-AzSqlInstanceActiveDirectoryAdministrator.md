---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 8a034bc85209e0325547bac2f64f277ceaee0abc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773760"
---
# <span data-ttu-id="cef88-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cef88-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="cef88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cef88-102">SYNOPSIS</span></span>
<span data-ttu-id="cef88-103">Provisiona uma instância gerenciada do Azure AD Administrator para SQL.</span><span class="sxs-lookup"><span data-stu-id="cef88-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="cef88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cef88-104">SYNTAX</span></span>

### <span data-ttu-id="cef88-105">UseResourceGroupAndInstanceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cef88-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef88-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef88-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cef88-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef88-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef88-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cef88-108">DESCRIPTION</span></span>
<span data-ttu-id="cef88-109">O cmdlet **set-AzSqlInstanceActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para AzureSQL instância gerenciada na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cef88-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="cef88-110">Você pode provisionar apenas um administrador de cada vez.</span><span class="sxs-lookup"><span data-stu-id="cef88-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="cef88-111">Os seguintes membros do Azure AD podem ser provisionados como um administrador de instância gerenciada SQL:</span><span class="sxs-lookup"><span data-stu-id="cef88-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="cef88-112">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="cef88-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="cef88-113">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="cef88-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="cef88-114">Grupos do Azure AD criados como grupos de segurança importados os membros de outros anúncios do Azure não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="cef88-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="cef88-115">Contas da Microsoft, como os dos domínios Outlook.com, Hotmail.com ou Live.com, não são compatíveis com administradores.</span><span class="sxs-lookup"><span data-stu-id="cef88-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="cef88-116">Não há suporte para outras contas de convidado, como aquelas dos domínios Gmail.com ou Yahoo.com como administradores.</span><span class="sxs-lookup"><span data-stu-id="cef88-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="cef88-117">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="cef88-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="cef88-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cef88-118">EXAMPLES</span></span>

### <span data-ttu-id="cef88-119">Exemplo 1: provisionar um grupo de administradores para uma instância gerenciada associada ao grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cef88-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="cef88-120">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para a instância gerenciada chamada ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="cef88-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="cef88-121">Este servidor está associado à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cef88-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="cef88-122">Exemplo 2: prover um usuário administrador usando o objeto da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="cef88-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="cef88-123">Este comando provisiona um usuário do Azure AD como administrador a partir do objeto de instância gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cef88-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="cef88-124">Exemplo 3: prover um administrador usando o identificador de recursos de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="cef88-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="cef88-125">Este comando provisiona um usuário do Azure AD como administrador usando o identificador de recursos de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="cef88-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="cef88-126">OS</span><span class="sxs-lookup"><span data-stu-id="cef88-126">PARAMETERS</span></span>

### <span data-ttu-id="cef88-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef88-127">-DefaultProfile</span></span>
<span data-ttu-id="cef88-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cef88-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef88-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cef88-129">-DisplayName</span></span>
<span data-ttu-id="cef88-130">Especifica o nome de exibição do usuário ou grupo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="cef88-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="cef88-131">Este nome para exibição deve existir no Active Directory associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cef88-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef88-132">-InputObject</span></span>
<span data-ttu-id="cef88-133">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="cef88-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cef88-134">-InstanceName</span></span>
<span data-ttu-id="cef88-135">Nome da instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="cef88-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cef88-136">-ObjectId</span></span>
<span data-ttu-id="cef88-137">Especifica a ID de objeto do usuário ou grupo no Azure Active Directory ao qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="cef88-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef88-138">-ResourceGroupName</span></span>
<span data-ttu-id="cef88-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cef88-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef88-140">-ResourceId</span></span>
<span data-ttu-id="cef88-141">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="cef88-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef88-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cef88-142">-Confirm</span></span>
<span data-ttu-id="cef88-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef88-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef88-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef88-144">-WhatIf</span></span>
<span data-ttu-id="cef88-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cef88-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef88-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cef88-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef88-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef88-147">CommonParameters</span></span>
<span data-ttu-id="cef88-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef88-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef88-149">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cef88-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef88-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cef88-150">INPUTS</span></span>

### <span data-ttu-id="cef88-151">System. String</span><span class="sxs-lookup"><span data-stu-id="cef88-151">System.String</span></span>

### <span data-ttu-id="cef88-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cef88-152">System.Guid</span></span>

## <span data-ttu-id="cef88-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cef88-153">OUTPUTS</span></span>

### <span data-ttu-id="cef88-154">Microsoft. Azure. Commands. Sql. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="cef88-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="cef88-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cef88-155">NOTES</span></span>

## <span data-ttu-id="cef88-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cef88-156">RELATED LINKS</span></span>

[<span data-ttu-id="cef88-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cef88-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="cef88-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cef88-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
