---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 174bccd7b682c1c4922a5ca7b6bbfbd406667df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427769"
---
# <span data-ttu-id="98f9b-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="98f9b-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="98f9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="98f9b-103">Obtém o protetor de criptografia de dados transparente (TDE)</span><span class="sxs-lookup"><span data-stu-id="98f9b-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98f9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f9b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="98f9b-106">O cmdlet Get-AzureRmSqlServerTransparentDataEncryptionProtector Obtém informações sobre o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="98f9b-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="98f9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="98f9b-108">--------------------------Exemplo 1: obter o protetor de criptografia de dados transparente (TDE)--------------------------</span><span class="sxs-lookup"><span data-stu-id="98f9b-108">--------------------------  Example 1: Get the Transparent Data Encryption (TDE) protector  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="98f9b-109">Esse comando obtém o protetor TDE do servidor chamado ContosoServer no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="98f9b-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="98f9b-110">Tipo de ResourceGroupName nomedoservidor ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="98f9b-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="98f9b-111">ContosoResourceGroup ContosoServerd não gerenciado pela</span><span class="sxs-lookup"><span data-stu-id="98f9b-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="98f9b-112">OS</span><span class="sxs-lookup"><span data-stu-id="98f9b-112">PARAMETERS</span></span>

### <span data-ttu-id="98f9b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f9b-113">-ResourceGroupName</span></span>
<span data-ttu-id="98f9b-114">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="98f9b-114">The name of the resource group</span></span>

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

### <span data-ttu-id="98f9b-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="98f9b-115">-ServerName</span></span>
<span data-ttu-id="98f9b-116">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="98f9b-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="98f9b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98f9b-117">-Confirm</span></span>
<span data-ttu-id="98f9b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f9b-119">-WhatIf</span></span>
<span data-ttu-id="98f9b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98f9b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f9b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98f9b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f9b-122">-DefaultProfile</span></span>
<span data-ttu-id="98f9b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98f9b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f9b-124">CommonParameters</span></span>
<span data-ttu-id="98f9b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f9b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f9b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98f9b-127">INPUTS</span></span>

### <span data-ttu-id="98f9b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98f9b-128">System.String</span></span>

## <span data-ttu-id="98f9b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98f9b-129">OUTPUTS</span></span>

### <span data-ttu-id="98f9b-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="98f9b-130">System.Object</span></span>

## <span data-ttu-id="98f9b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98f9b-131">NOTES</span></span>

## <span data-ttu-id="98f9b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98f9b-132">RELATED LINKS</span></span>

[<span data-ttu-id="98f9b-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="98f9b-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)