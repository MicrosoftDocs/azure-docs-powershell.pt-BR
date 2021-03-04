---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888159"
---
# <span data-ttu-id="e5b76-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="e5b76-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="e5b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b76-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b76-103">Obtém política avançada de Segurança de Dados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e5b76-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="e5b76-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5b76-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5b76-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5b76-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b76-106">O cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera a política de Segurança de Dados Avançada de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e5b76-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="e5b76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5b76-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b76-108">Exemplo 1: obtém segurança avançada de dados do servidor</span><span class="sxs-lookup"><span data-stu-id="e5b76-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="e5b76-109">Exemplo 2: Obtém a Segurança Avançada de Dados do servidor a partir do recurso de servidor</span><span class="sxs-lookup"><span data-stu-id="e5b76-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="e5b76-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5b76-110">PARAMETERS</span></span>

### <span data-ttu-id="e5b76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b76-111">-DefaultProfile</span></span>
<span data-ttu-id="e5b76-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b76-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b76-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b76-113">-InputObject</span></span>
<span data-ttu-id="e5b76-114">O objeto server a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="e5b76-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b76-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b76-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5b76-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5b76-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5b76-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5b76-117">-ServerName</span></span>
<span data-ttu-id="e5b76-118">SQL nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e5b76-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="e5b76-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b76-119">CommonParameters</span></span>
<span data-ttu-id="e5b76-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b76-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b76-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5b76-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b76-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b76-122">INPUTS</span></span>

### <span data-ttu-id="e5b76-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e5b76-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="e5b76-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b76-124">System.String</span></span>

## <span data-ttu-id="e5b76-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5b76-125">OUTPUTS</span></span>

### <span data-ttu-id="e5b76-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e5b76-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="e5b76-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5b76-127">NOTES</span></span>

## <span data-ttu-id="e5b76-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5b76-128">RELATED LINKS</span></span>
