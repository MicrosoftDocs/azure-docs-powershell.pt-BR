---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599057"
---
# <span data-ttu-id="f2c3f-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f2c3f-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="f2c3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c3f-103">Habilita a proteção avançada contra ameaças em um servidor.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="f2c3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2c3f-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2c3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c3f-106">O cmdlet **Enable-AzSqlServerAdvancedThreatProtection** habilita a proteção avançada contra ameaças em um servidor.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="f2c3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2c3f-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c3f-108">Exemplo 1-habilitar a proteção avançada contra ameaças do servidor</span><span class="sxs-lookup"><span data-stu-id="f2c3f-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="f2c3f-109">Exemplo 2-habilitar a proteção avançada contra ameaças do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="f2c3f-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="f2c3f-110">OS</span><span class="sxs-lookup"><span data-stu-id="f2c3f-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c3f-111">-DefaultProfile</span></span>
<span data-ttu-id="f2c3f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2c3f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2c3f-113">-InputObject</span></span>
<span data-ttu-id="f2c3f-114">O objeto de servidor a ser usado com a operação avançada de política de proteção contra ameaças</span><span class="sxs-lookup"><span data-stu-id="f2c3f-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="f2c3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2c3f-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2c3f-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f2c3f-117">-ServerName</span></span>
<span data-ttu-id="f2c3f-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="f2c3f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2c3f-119">-Confirm</span></span>
<span data-ttu-id="f2c3f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2c3f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2c3f-121">-WhatIf</span></span>
<span data-ttu-id="f2c3f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2c3f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2c3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c3f-124">CommonParameters</span></span>
<span data-ttu-id="f2c3f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c3f-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2c3f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c3f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2c3f-127">INPUTS</span></span>

### <span data-ttu-id="f2c3f-128">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f2c3f-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="f2c3f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2c3f-129">System.String</span></span>

## <span data-ttu-id="f2c3f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2c3f-130">OUTPUTS</span></span>

### <span data-ttu-id="f2c3f-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f2c3f-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="f2c3f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2c3f-132">NOTES</span></span>

## <span data-ttu-id="f2c3f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2c3f-133">RELATED LINKS</span></span>
