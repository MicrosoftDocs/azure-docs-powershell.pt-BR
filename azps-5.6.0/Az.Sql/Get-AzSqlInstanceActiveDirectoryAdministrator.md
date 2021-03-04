---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 0638e44f9f1c8febcbb9700fce1b9c4c9d5e410c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901396"
---
# <span data-ttu-id="8a4a7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8a4a7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8a4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4a7-103">Obtém informações sobre um administrador do Azure AD para SQL Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="8a4a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8a4a7-104">SYNTAX</span></span>

### <span data-ttu-id="8a4a7-105">UseResourceGroupAndInstanceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a4a7-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4a7-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a4a7-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4a7-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4a7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8a4a7-108">DESCRIPTION</span></span>
<span data-ttu-id="8a4a7-109">O cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** obtém informações sobre um administrador do Azure Active Directory (Azure AD) para uma Instância Gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="8a4a7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-110">EXAMPLES</span></span>

### <span data-ttu-id="8a4a7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a4a7-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8a4a7-112">Este comando obtém informações sobre um administrador do Azure AD para uma instância gerenciada chamada ManagedInstance01 associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="8a4a7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a4a7-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8a4a7-114">Este comando obtém informações sobre um administrador do Azure AD de um objeto de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="8a4a7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8a4a7-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="8a4a7-116">Este comando obtém informações sobre um administrador do Azure AD usando o identificador de recurso de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="8a4a7-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-117">PARAMETERS</span></span>

### <span data-ttu-id="8a4a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4a7-118">-DefaultProfile</span></span>
<span data-ttu-id="8a4a7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4a7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4a7-120">-InputObject</span></span>
<span data-ttu-id="8a4a7-121">O objeto de instância gerenciada a ser usado.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="8a4a7-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8a4a7-122">-InstanceName</span></span>
<span data-ttu-id="8a4a7-123">SQL nome da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="8a4a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a4a7-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8a4a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4a7-126">-ResourceId</span></span>
<span data-ttu-id="8a4a7-127">A id de recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="8a4a7-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="8a4a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4a7-128">CommonParameters</span></span>
<span data-ttu-id="8a4a7-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4a7-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4a7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-131">INPUTS</span></span>

### <span data-ttu-id="8a4a7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8a4a7-132">System.String</span></span>

## <span data-ttu-id="8a4a7-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-133">OUTPUTS</span></span>

### <span data-ttu-id="8a4a7-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="8a4a7-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="8a4a7-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="8a4a7-135">NOTES</span></span>

## <span data-ttu-id="8a4a7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a4a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="8a4a7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8a4a7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="8a4a7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8a4a7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
