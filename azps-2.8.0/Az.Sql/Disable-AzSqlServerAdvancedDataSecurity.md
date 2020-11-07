---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: ca3b39ac369900f19c41b27b50efb06af7cf2056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773498"
---
# <span data-ttu-id="af9fb-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="af9fb-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="af9fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="af9fb-103">Desabilita a segurança avançada de dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="af9fb-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="af9fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af9fb-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af9fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="af9fb-106">O cmdlet **Disable-AzSqlServerAdvancedDataSecurity** desabilita a segurança avançada de dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="af9fb-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="af9fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af9fb-107">EXAMPLES</span></span>

### <span data-ttu-id="af9fb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af9fb-108">Example 1</span></span>
### <span data-ttu-id="af9fb-109">Exemplo 1-desabilitar a segurança de dados avançados do servidor</span><span class="sxs-lookup"><span data-stu-id="af9fb-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="af9fb-110">Exemplo 2-desabilitar a segurança de dados avançados do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="af9fb-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="af9fb-111">OS</span><span class="sxs-lookup"><span data-stu-id="af9fb-111">PARAMETERS</span></span>

### <span data-ttu-id="af9fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9fb-112">-DefaultProfile</span></span>
<span data-ttu-id="af9fb-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af9fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9fb-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9fb-114">-InputObject</span></span>
<span data-ttu-id="af9fb-115">O objeto de servidor a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="af9fb-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="af9fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="af9fb-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af9fb-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="af9fb-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="af9fb-118">-ServerName</span></span>
<span data-ttu-id="af9fb-119">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="af9fb-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="af9fb-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af9fb-120">-Confirm</span></span>
<span data-ttu-id="af9fb-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af9fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9fb-122">-WhatIf</span></span>
<span data-ttu-id="af9fb-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af9fb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9fb-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af9fb-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9fb-125">CommonParameters</span></span>
<span data-ttu-id="af9fb-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="af9fb-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9fb-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af9fb-128">INPUTS</span></span>

### <span data-ttu-id="af9fb-129">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="af9fb-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="af9fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af9fb-130">System.String</span></span>

## <span data-ttu-id="af9fb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af9fb-131">OUTPUTS</span></span>

### <span data-ttu-id="af9fb-132">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="af9fb-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="af9fb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af9fb-133">NOTES</span></span>

## <span data-ttu-id="af9fb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af9fb-134">RELATED LINKS</span></span>