---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281586"
---
# <span data-ttu-id="c27c8-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c27c8-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="c27c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c27c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c27c8-103">Obtém a autenticação do Azure AD apenas para uma instância específica de SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="c27c8-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="c27c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c27c8-104">SYNTAX</span></span>

### <span data-ttu-id="c27c8-105">UseResourceGroupAndInstanceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c27c8-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c27c8-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c27c8-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c27c8-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c27c8-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c27c8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c27c8-108">DESCRIPTION</span></span>
<span data-ttu-id="c27c8-109">O cmdlet **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** Obtém o Azure Active Directory (Azure AD) apenas requisito de autenticação para uma instância gerenciada AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c27c8-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="c27c8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c27c8-110">EXAMPLES</span></span>

### <span data-ttu-id="c27c8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c27c8-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="c27c8-112">Este comando obtém o Azure Active Directory (Azure AD) apenas requisito de autenticação para uma instância gerenciada AzureSQL chamada ManagedInstance01 que está associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c27c8-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c27c8-113">OS</span><span class="sxs-lookup"><span data-stu-id="c27c8-113">PARAMETERS</span></span>

### <span data-ttu-id="c27c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27c8-114">-DefaultProfile</span></span>
<span data-ttu-id="c27c8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c27c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c27c8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c27c8-116">-InputObject</span></span>
<span data-ttu-id="c27c8-117">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c27c8-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="c27c8-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c27c8-118">-InstanceName</span></span>
<span data-ttu-id="c27c8-119">O nome da instância gerenciada SQL do Azure a única autenticação do Azure Active Directory está em.</span><span class="sxs-lookup"><span data-stu-id="c27c8-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="c27c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c27c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="c27c8-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c27c8-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="c27c8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c27c8-122">-ResourceId</span></span>
<span data-ttu-id="c27c8-123">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="c27c8-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="c27c8-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c27c8-124">-Confirm</span></span>
<span data-ttu-id="c27c8-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c27c8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c27c8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c27c8-126">-WhatIf</span></span>
<span data-ttu-id="c27c8-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c27c8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c27c8-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c27c8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c27c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27c8-129">CommonParameters</span></span>
<span data-ttu-id="c27c8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27c8-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c27c8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27c8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c27c8-132">INPUTS</span></span>

### <span data-ttu-id="c27c8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c27c8-133">System.String</span></span>

## <span data-ttu-id="c27c8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c27c8-134">OUTPUTS</span></span>

### <span data-ttu-id="c27c8-135">Microsoft. Azure. Commands. Sql. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="c27c8-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="c27c8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c27c8-136">NOTES</span></span>

## <span data-ttu-id="c27c8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c27c8-137">RELATED LINKS</span></span>

[<span data-ttu-id="c27c8-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c27c8-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c27c8-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c27c8-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c27c8-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c27c8-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="c27c8-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c27c8-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

