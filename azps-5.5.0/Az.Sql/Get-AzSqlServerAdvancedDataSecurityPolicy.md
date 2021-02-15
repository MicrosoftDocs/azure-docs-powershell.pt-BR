---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114480"
---
# <span data-ttu-id="25459-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="25459-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="25459-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25459-102">SYNOPSIS</span></span>
<span data-ttu-id="25459-103">Obtém uma política de Segurança de Dados Avançada de um servidor.</span><span class="sxs-lookup"><span data-stu-id="25459-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="25459-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25459-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25459-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="25459-105">DESCRIPTION</span></span>
<span data-ttu-id="25459-106">O cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera a política de Segurança de Dados Avançada de um servidor.</span><span class="sxs-lookup"><span data-stu-id="25459-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="25459-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25459-107">EXAMPLES</span></span>

### <span data-ttu-id="25459-108">Exemplo 1: Obtém segurança avançada de dados do servidor</span><span class="sxs-lookup"><span data-stu-id="25459-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="25459-109">Exemplo 2: obtém a Segurança de Dados Avançada do servidor do recurso de servidor</span><span class="sxs-lookup"><span data-stu-id="25459-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="25459-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25459-110">PARAMETERS</span></span>

### <span data-ttu-id="25459-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25459-111">-DefaultProfile</span></span>
<span data-ttu-id="25459-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25459-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25459-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25459-113">-InputObject</span></span>
<span data-ttu-id="25459-114">O objeto do servidor a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="25459-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="25459-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25459-115">-ResourceGroupName</span></span>
<span data-ttu-id="25459-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25459-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="25459-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25459-117">-ServerName</span></span>
<span data-ttu-id="25459-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="25459-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="25459-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25459-119">CommonParameters</span></span>
<span data-ttu-id="25459-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25459-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25459-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25459-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25459-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="25459-122">INPUTS</span></span>

### <span data-ttu-id="25459-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="25459-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="25459-124">System.String</span><span class="sxs-lookup"><span data-stu-id="25459-124">System.String</span></span>

## <span data-ttu-id="25459-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="25459-125">OUTPUTS</span></span>

### <span data-ttu-id="25459-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="25459-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="25459-127">Notas</span><span class="sxs-lookup"><span data-stu-id="25459-127">NOTES</span></span>

## <span data-ttu-id="25459-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25459-128">RELATED LINKS</span></span>
