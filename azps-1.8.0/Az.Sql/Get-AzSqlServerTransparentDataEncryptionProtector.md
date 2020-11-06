---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: c1571dd5d03f82da13feec115fb9da123c6e3f69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598931"
---
# <span data-ttu-id="61dab-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="61dab-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="61dab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61dab-102">SYNOPSIS</span></span>
<span data-ttu-id="61dab-103">Obtém o protetor de criptografia de dados transparente (TDE)</span><span class="sxs-lookup"><span data-stu-id="61dab-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="61dab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61dab-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61dab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61dab-105">DESCRIPTION</span></span>
<span data-ttu-id="61dab-106">O cmdlet Get-AzSqlServerTransparentDataEncryptionProtector Obtém informações sobre o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="61dab-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="61dab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61dab-107">EXAMPLES</span></span>

### <span data-ttu-id="61dab-108">Exemplo 1: obter o protetor de criptografia de dados transparente (TDE)</span><span class="sxs-lookup"><span data-stu-id="61dab-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="61dab-109">Esse comando obtém o protetor TDE do servidor chamado ContosoServer no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61dab-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="61dab-110">Tipo de ResourceGroupName nomedoservidor ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="61dab-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="61dab-111">ContosoResourceGroup ContosoServerd não gerenciado pela</span><span class="sxs-lookup"><span data-stu-id="61dab-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="61dab-112">OS</span><span class="sxs-lookup"><span data-stu-id="61dab-112">PARAMETERS</span></span>

### <span data-ttu-id="61dab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dab-113">-DefaultProfile</span></span>
<span data-ttu-id="61dab-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="61dab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61dab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61dab-115">-ResourceGroupName</span></span>
<span data-ttu-id="61dab-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61dab-116">The name of the resource group</span></span>

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

### <span data-ttu-id="61dab-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="61dab-117">-ServerName</span></span>
<span data-ttu-id="61dab-118">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="61dab-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="61dab-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61dab-119">-Confirm</span></span>
<span data-ttu-id="61dab-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61dab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dab-121">-WhatIf</span></span>
<span data-ttu-id="61dab-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61dab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61dab-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61dab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dab-124">CommonParameters</span></span>
<span data-ttu-id="61dab-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dab-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61dab-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dab-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61dab-127">INPUTS</span></span>

### <span data-ttu-id="61dab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61dab-128">System.String</span></span>

## <span data-ttu-id="61dab-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61dab-129">OUTPUTS</span></span>

### <span data-ttu-id="61dab-130">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="61dab-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="61dab-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61dab-131">NOTES</span></span>

## <span data-ttu-id="61dab-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61dab-132">RELATED LINKS</span></span>

[<span data-ttu-id="61dab-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="61dab-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
