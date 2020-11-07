---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 74956ff74beeb166a7788d0e577a86a4d2538ded
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773607"
---
# <span data-ttu-id="81822-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="81822-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="81822-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81822-102">SYNOPSIS</span></span>
<span data-ttu-id="81822-103">Obtém a política de segurança de dados avançada de um servidor.</span><span class="sxs-lookup"><span data-stu-id="81822-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="81822-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81822-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81822-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81822-105">DESCRIPTION</span></span>
<span data-ttu-id="81822-106">O cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera a política de segurança de dados avançada de um servidor.</span><span class="sxs-lookup"><span data-stu-id="81822-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="81822-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81822-107">EXAMPLES</span></span>

### <span data-ttu-id="81822-108">Exemplo 1-obtém segurança de dados avançados do servidor</span><span class="sxs-lookup"><span data-stu-id="81822-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="81822-109">Exemplo 2-obtém segurança de dados avançada do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="81822-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="81822-110">OS</span><span class="sxs-lookup"><span data-stu-id="81822-110">PARAMETERS</span></span>

### <span data-ttu-id="81822-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81822-111">-DefaultProfile</span></span>
<span data-ttu-id="81822-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81822-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81822-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81822-113">-InputObject</span></span>
<span data-ttu-id="81822-114">O objeto de servidor a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="81822-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81822-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81822-115">-ResourceGroupName</span></span>
<span data-ttu-id="81822-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81822-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81822-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="81822-117">-ServerName</span></span>
<span data-ttu-id="81822-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="81822-118">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81822-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81822-119">CommonParameters</span></span>
<span data-ttu-id="81822-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81822-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="81822-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81822-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81822-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81822-122">INPUTS</span></span>

### <span data-ttu-id="81822-123">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="81822-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="81822-124">System. String</span><span class="sxs-lookup"><span data-stu-id="81822-124">System.String</span></span>

## <span data-ttu-id="81822-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81822-125">OUTPUTS</span></span>

### <span data-ttu-id="81822-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="81822-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="81822-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81822-127">NOTES</span></span>

## <span data-ttu-id="81822-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81822-128">RELATED LINKS</span></span>
