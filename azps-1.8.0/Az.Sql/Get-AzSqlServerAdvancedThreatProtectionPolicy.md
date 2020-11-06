---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598956"
---
# <span data-ttu-id="99def-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="99def-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="99def-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99def-102">SYNOPSIS</span></span>
<span data-ttu-id="99def-103">Obtém uma política avançada de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="99def-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="99def-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99def-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99def-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99def-105">DESCRIPTION</span></span>
<span data-ttu-id="99def-106">O cmdlet **Get-AzSqlServerAdvancedThreatProtectionPolicy** Retrives a política avançada de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="99def-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="99def-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99def-107">EXAMPLES</span></span>

### <span data-ttu-id="99def-108">Exemplo 1-obtém proteção avançada contra ameaças do servidor</span><span class="sxs-lookup"><span data-stu-id="99def-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="99def-109">Exemplo 2-obtém proteção avançada contra ameaças do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="99def-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="99def-110">OS</span><span class="sxs-lookup"><span data-stu-id="99def-110">PARAMETERS</span></span>

### <span data-ttu-id="99def-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99def-111">-DefaultProfile</span></span>
<span data-ttu-id="99def-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99def-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99def-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99def-113">-InputObject</span></span>
<span data-ttu-id="99def-114">O objeto de servidor a ser usado com a operação avançada de política de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="99def-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="99def-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99def-115">-ResourceGroupName</span></span>
<span data-ttu-id="99def-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99def-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="99def-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="99def-117">-ServerName</span></span>
<span data-ttu-id="99def-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="99def-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="99def-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99def-119">CommonParameters</span></span>
<span data-ttu-id="99def-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99def-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99def-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99def-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99def-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99def-122">INPUTS</span></span>

### <span data-ttu-id="99def-123">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="99def-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="99def-124">System. String</span><span class="sxs-lookup"><span data-stu-id="99def-124">System.String</span></span>

## <span data-ttu-id="99def-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99def-125">OUTPUTS</span></span>

### <span data-ttu-id="99def-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="99def-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="99def-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99def-127">NOTES</span></span>

## <span data-ttu-id="99def-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99def-128">RELATED LINKS</span></span>
