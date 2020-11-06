---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431879"
---
# <span data-ttu-id="5347f-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5347f-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="5347f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5347f-102">SYNOPSIS</span></span>
<span data-ttu-id="5347f-103">Obtém uma política avançada de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5347f-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5347f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5347f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5347f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5347f-105">DESCRIPTION</span></span>
<span data-ttu-id="5347f-106">O cmdlet **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** Retrives a política avançada de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5347f-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="5347f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5347f-107">EXAMPLES</span></span>

### <span data-ttu-id="5347f-108">Exemplo 1-obtém proteção avançada contra ameaças do servidor</span><span class="sxs-lookup"><span data-stu-id="5347f-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="5347f-109">Exemplo 2-obtém proteção avançada contra ameaças do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="5347f-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="5347f-110">OS</span><span class="sxs-lookup"><span data-stu-id="5347f-110">PARAMETERS</span></span>

### <span data-ttu-id="5347f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5347f-111">-DefaultProfile</span></span>
<span data-ttu-id="5347f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5347f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5347f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5347f-113">-InputObject</span></span>
<span data-ttu-id="5347f-114">O objeto de servidor a ser usado com a operação avançada de política de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="5347f-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="5347f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5347f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5347f-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5347f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5347f-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5347f-117">-ServerName</span></span>
<span data-ttu-id="5347f-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="5347f-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5347f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5347f-119">CommonParameters</span></span>
<span data-ttu-id="5347f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5347f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5347f-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5347f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5347f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5347f-122">INPUTS</span></span>

### <span data-ttu-id="5347f-123">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5347f-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="5347f-124">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5347f-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5347f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5347f-125">System.String</span></span>

## <span data-ttu-id="5347f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5347f-126">OUTPUTS</span></span>

### <span data-ttu-id="5347f-127">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5347f-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5347f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5347f-128">NOTES</span></span>

## <span data-ttu-id="5347f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5347f-129">RELATED LINKS</span></span>
