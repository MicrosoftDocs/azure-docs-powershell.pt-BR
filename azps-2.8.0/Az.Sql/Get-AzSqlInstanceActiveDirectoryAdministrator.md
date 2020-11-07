---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 6a1d69beaf6178326376278788cef612bf71c15f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773897"
---
# <span data-ttu-id="6f105-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6f105-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6f105-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f105-102">SYNOPSIS</span></span>
<span data-ttu-id="6f105-103">Obtém informações sobre uma instância gerenciada do Azure AD Administrator para SQL.</span><span class="sxs-lookup"><span data-stu-id="6f105-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="6f105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f105-104">SYNTAX</span></span>

### <span data-ttu-id="6f105-105">UseResourceGroupAndInstanceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f105-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f105-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f105-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-InputObject <AzureSqlManagedInstanceModel>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f105-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f105-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f105-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f105-108">DESCRIPTION</span></span>
<span data-ttu-id="6f105-109">O cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** Obtém informações sobre um administrador do Azure Active Directory (Azure AD) para uma instância gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6f105-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="6f105-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f105-110">EXAMPLES</span></span>

### <span data-ttu-id="6f105-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f105-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6f105-112">Esse comando obtém informações sobre um administrador do Azure AD para uma instância gerenciada chamada ManagedInstance01 que está associada a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6f105-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="6f105-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f105-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6f105-114">Esse comando obtém informações sobre um administrador do Azure AD a partir de um objeto de instância gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6f105-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="6f105-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6f105-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6f105-116">Esse comando obtém informações sobre um administrador do Azure AD usando o identificador de recursos de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6f105-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="6f105-117">OS</span><span class="sxs-lookup"><span data-stu-id="6f105-117">PARAMETERS</span></span>

### <span data-ttu-id="6f105-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f105-118">-DefaultProfile</span></span>
<span data-ttu-id="6f105-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f105-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f105-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f105-120">-InputObject</span></span>
<span data-ttu-id="6f105-121">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="6f105-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="6f105-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6f105-122">-InstanceName</span></span>
<span data-ttu-id="6f105-123">Nome da instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="6f105-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="6f105-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f105-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f105-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f105-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f105-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f105-126">-ResourceId</span></span>
<span data-ttu-id="6f105-127">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="6f105-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="6f105-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f105-128">CommonParameters</span></span>
<span data-ttu-id="6f105-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f105-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f105-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f105-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f105-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f105-131">INPUTS</span></span>

### <span data-ttu-id="6f105-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f105-132">System.String</span></span>

## <span data-ttu-id="6f105-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f105-133">OUTPUTS</span></span>

### <span data-ttu-id="6f105-134">Microsoft. Azure. Commands. Sql. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="6f105-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="6f105-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f105-135">NOTES</span></span>

## <span data-ttu-id="6f105-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f105-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f105-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6f105-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="6f105-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6f105-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
