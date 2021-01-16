---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258060"
---
# <span data-ttu-id="2e953-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e953-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="2e953-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e953-102">SYNOPSIS</span></span>
<span data-ttu-id="2e953-103">Habilita a autenticação do Azure AD somente para uma instância específica de SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="2e953-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="2e953-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e953-104">SYNTAX</span></span>

### <span data-ttu-id="2e953-105">UseResourceGroupAndInstanceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e953-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e953-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e953-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e953-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e953-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e953-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e953-108">DESCRIPTION</span></span>
<span data-ttu-id="2e953-109">O cmdlet **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** habilita o Azure Active Directory (Azure AD) apenas requisito de autenticação para uma instância gerenciada AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="2e953-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="2e953-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e953-110">EXAMPLES</span></span>

### <span data-ttu-id="2e953-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e953-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="2e953-112">Esse comando habilita o Azure Active Directory (Azure AD) apenas requisito de autenticação para uma instância gerenciada AzureSQL chamada ManagedInstance01 que está associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2e953-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2e953-113">OS</span><span class="sxs-lookup"><span data-stu-id="2e953-113">PARAMETERS</span></span>

### <span data-ttu-id="2e953-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e953-114">-DefaultProfile</span></span>
<span data-ttu-id="2e953-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e953-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e953-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e953-116">-InputObject</span></span>
<span data-ttu-id="2e953-117">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="2e953-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="2e953-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2e953-118">-InstanceName</span></span>
<span data-ttu-id="2e953-119">O nome da instância gerenciada SQL do Azure a única autenticação do Azure Active Directory está em.</span><span class="sxs-lookup"><span data-stu-id="2e953-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="2e953-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e953-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e953-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e953-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e953-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e953-122">-ResourceId</span></span>
<span data-ttu-id="2e953-123">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="2e953-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="2e953-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e953-124">-Confirm</span></span>
<span data-ttu-id="2e953-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e953-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e953-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e953-126">-WhatIf</span></span>
<span data-ttu-id="2e953-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e953-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e953-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e953-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e953-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e953-129">CommonParameters</span></span>
<span data-ttu-id="2e953-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e953-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e953-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e953-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e953-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e953-132">INPUTS</span></span>

### <span data-ttu-id="2e953-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2e953-133">System.String</span></span>

## <span data-ttu-id="2e953-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e953-134">OUTPUTS</span></span>

### <span data-ttu-id="2e953-135">Microsoft. Azure. Commands. Sql. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="2e953-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="2e953-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e953-136">NOTES</span></span>

## <span data-ttu-id="2e953-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e953-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e953-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e953-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="2e953-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="2e953-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="2e953-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2e953-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="2e953-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2e953-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)