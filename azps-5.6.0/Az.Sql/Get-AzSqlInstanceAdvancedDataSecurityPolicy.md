---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 2d9fa7ef7d3763d2db1d963aa1b1cac41b711bd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901390"
---
# <span data-ttu-id="318ba-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="318ba-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="318ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="318ba-102">SYNOPSIS</span></span>
<span data-ttu-id="318ba-103">Obtém a política de Segurança de Dados Avançada de uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="318ba-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="318ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="318ba-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="318ba-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="318ba-105">DESCRIPTION</span></span>
<span data-ttu-id="318ba-106">O cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** recupera a política de Segurança de Dados Avançada de uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="318ba-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="318ba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="318ba-107">EXAMPLES</span></span>

### <span data-ttu-id="318ba-108">Exemplo 1: obtém instância gerenciada Segurança avançada de dados</span><span class="sxs-lookup"><span data-stu-id="318ba-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="318ba-109">Exemplo 2: obtém instância gerenciada Segurança avançada de dados do recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="318ba-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="318ba-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="318ba-110">PARAMETERS</span></span>

### <span data-ttu-id="318ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318ba-111">-DefaultProfile</span></span>
<span data-ttu-id="318ba-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="318ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318ba-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="318ba-113">-InputObject</span></span>
<span data-ttu-id="318ba-114">O objeto de instância gerenciada a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="318ba-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="318ba-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="318ba-115">-InstanceName</span></span>
<span data-ttu-id="318ba-116">SQL nome da instância gerenciada do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="318ba-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="318ba-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="318ba-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318ba-119">CommonParameters</span></span>
<span data-ttu-id="318ba-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318ba-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="318ba-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318ba-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="318ba-122">INPUTS</span></span>

### <span data-ttu-id="318ba-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="318ba-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="318ba-124">System.String</span><span class="sxs-lookup"><span data-stu-id="318ba-124">System.String</span></span>

## <span data-ttu-id="318ba-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="318ba-125">OUTPUTS</span></span>

### <span data-ttu-id="318ba-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="318ba-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="318ba-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="318ba-127">NOTES</span></span>

## <span data-ttu-id="318ba-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318ba-128">RELATED LINKS</span></span>
