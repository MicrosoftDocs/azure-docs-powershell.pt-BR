---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: cd211537949fe3743298ad4cba93ca6c63b7c39b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892036"
---
# <span data-ttu-id="6d237-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6d237-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="6d237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d237-102">SYNOPSIS</span></span>
<span data-ttu-id="6d237-103">Obtém o protetor TDE (Criptografia de Dados Transparentes)</span><span class="sxs-lookup"><span data-stu-id="6d237-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="6d237-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d237-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d237-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d237-105">DESCRIPTION</span></span>
<span data-ttu-id="6d237-106">O Get-AzSqlServerTransparentDataEncryptionProtector cmdlet obtém informações sobre o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="6d237-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="6d237-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d237-107">EXAMPLES</span></span>

### <span data-ttu-id="6d237-108">Exemplo 1: Obter o protetor TDE (Criptografia de Dados Transparente)</span><span class="sxs-lookup"><span data-stu-id="6d237-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="6d237-109">Este comando obtém o protetor TDE para o servidor chamado ContosoServer no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6d237-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="6d237-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="6d237-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="6d237-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="6d237-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="6d237-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d237-112">PARAMETERS</span></span>

### <span data-ttu-id="6d237-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d237-113">-DefaultProfile</span></span>
<span data-ttu-id="6d237-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6d237-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d237-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d237-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d237-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6d237-116">The name of the resource group</span></span>

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

### <span data-ttu-id="6d237-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6d237-117">-ServerName</span></span>
<span data-ttu-id="6d237-118">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d237-118">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d237-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d237-119">-Confirm</span></span>
<span data-ttu-id="6d237-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d237-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d237-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d237-121">-WhatIf</span></span>
<span data-ttu-id="6d237-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d237-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d237-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d237-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d237-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d237-124">CommonParameters</span></span>
<span data-ttu-id="6d237-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d237-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d237-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d237-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d237-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d237-127">INPUTS</span></span>

### <span data-ttu-id="6d237-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6d237-128">System.String</span></span>

## <span data-ttu-id="6d237-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d237-129">OUTPUTS</span></span>

### <span data-ttu-id="6d237-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="6d237-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="6d237-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d237-131">NOTES</span></span>

## <span data-ttu-id="6d237-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d237-132">RELATED LINKS</span></span>

[<span data-ttu-id="6d237-133">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="6d237-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
