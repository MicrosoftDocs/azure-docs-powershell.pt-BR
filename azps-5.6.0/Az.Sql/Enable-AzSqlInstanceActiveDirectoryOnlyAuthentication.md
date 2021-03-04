---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: c96b1b9a7eb715f2ab7f02c7e3f86191ac756296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890580"
---
# <span data-ttu-id="4e313-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4e313-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="4e313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e313-102">SYNOPSIS</span></span>
<span data-ttu-id="4e313-103">Habilita a autenticação somente do Azure AD para uma instância SQL Gerenciada específica.</span><span class="sxs-lookup"><span data-stu-id="4e313-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="4e313-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e313-104">SYNTAX</span></span>

### <span data-ttu-id="4e313-105">UseResourceGroupAndInstanceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4e313-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e313-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e313-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e313-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e313-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e313-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e313-108">DESCRIPTION</span></span>
<span data-ttu-id="4e313-109">O cmdlet **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** permite que o Azure Active Directory (Azure AD) só seja requisito de autenticação para uma Instância Gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4e313-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="4e313-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e313-110">EXAMPLES</span></span>

### <span data-ttu-id="4e313-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e313-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="4e313-112">Esse comando habilita o Azure Active Directory (Azure AD) somente requisito de autenticação para uma Instância Gerenciada do AzureSQL chamada ManagedInstance01 associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4e313-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4e313-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e313-113">PARAMETERS</span></span>

### <span data-ttu-id="4e313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e313-114">-DefaultProfile</span></span>
<span data-ttu-id="4e313-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e313-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e313-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e313-116">-InputObject</span></span>
<span data-ttu-id="4e313-117">O objeto de instância gerenciada a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4e313-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e313-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4e313-118">-InstanceName</span></span>
<span data-ttu-id="4e313-119">O nome da instância gerenciada do Azure SQL a autenticação somente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e313-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="4e313-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e313-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e313-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e313-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e313-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e313-122">-ResourceId</span></span>
<span data-ttu-id="4e313-123">A id de recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="4e313-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="4e313-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e313-124">-Confirm</span></span>
<span data-ttu-id="4e313-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e313-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e313-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e313-126">-WhatIf</span></span>
<span data-ttu-id="4e313-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e313-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e313-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e313-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e313-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e313-129">CommonParameters</span></span>
<span data-ttu-id="4e313-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e313-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e313-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e313-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e313-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e313-132">INPUTS</span></span>

### <span data-ttu-id="4e313-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4e313-133">System.String</span></span>

## <span data-ttu-id="4e313-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e313-134">OUTPUTS</span></span>

### <span data-ttu-id="4e313-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="4e313-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="4e313-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e313-136">NOTES</span></span>

## <span data-ttu-id="4e313-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e313-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e313-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4e313-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4e313-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4e313-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4e313-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4e313-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="4e313-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4e313-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)