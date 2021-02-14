---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115768"
---
# <span data-ttu-id="f3346-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f3346-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f3346-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3346-102">SYNOPSIS</span></span>
<span data-ttu-id="f3346-103">Desabilita a autenticação somente do Azure AD para uma Instância Gerenciada do SQL específica.</span><span class="sxs-lookup"><span data-stu-id="f3346-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="f3346-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3346-104">SYNTAX</span></span>

### <span data-ttu-id="f3346-105">UseResourceGroupAndInstanceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f3346-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3346-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3346-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3346-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3346-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3346-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3346-108">DESCRIPTION</span></span>
<span data-ttu-id="f3346-109">O cmdlet **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** desabilita o requisito de autenticação somente do Azure Active Directory (Azure AD) para uma Instância Gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f3346-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="f3346-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3346-110">EXAMPLES</span></span>

### <span data-ttu-id="f3346-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3346-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="f3346-112">Esse comando desabilita o requisito somente de autenticação do Azure Active Directory (Azure AD) para uma Instância Gerenciada do AzureSQL chamada ManagedInstance01 associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f3346-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f3346-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3346-113">PARAMETERS</span></span>

### <span data-ttu-id="f3346-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3346-114">-DefaultProfile</span></span>
<span data-ttu-id="f3346-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3346-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3346-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3346-116">-InputObject</span></span>
<span data-ttu-id="f3346-117">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f3346-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="f3346-118">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="f3346-118">-InstanceName</span></span>
<span data-ttu-id="f3346-119">O nome da Instância Gerenciada do SQL do Azure na qual a autenticação somente do Azure Active Directory está.</span><span class="sxs-lookup"><span data-stu-id="f3346-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="f3346-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3346-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3346-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3346-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3346-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3346-122">-ResourceId</span></span>
<span data-ttu-id="f3346-123">A ID do recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="f3346-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="f3346-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f3346-124">-Confirm</span></span>
<span data-ttu-id="f3346-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3346-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3346-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3346-126">-WhatIf</span></span>
<span data-ttu-id="f3346-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f3346-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3346-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3346-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3346-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3346-129">CommonParameters</span></span>
<span data-ttu-id="f3346-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3346-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3346-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3346-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3346-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="f3346-132">INPUTS</span></span>

### <span data-ttu-id="f3346-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f3346-133">System.String</span></span>

## <span data-ttu-id="f3346-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="f3346-134">OUTPUTS</span></span>

### <span data-ttu-id="f3346-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="f3346-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="f3346-136">Notas</span><span class="sxs-lookup"><span data-stu-id="f3346-136">NOTES</span></span>

## <span data-ttu-id="f3346-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3346-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3346-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f3346-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f3346-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f3346-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f3346-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f3346-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="f3346-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f3346-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)