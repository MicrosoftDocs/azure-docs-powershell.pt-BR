---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432165"
---
# <span data-ttu-id="0b5a3-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5a3-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="0b5a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5a3-103">Especifica que um banco de dados usa a política de auditoria do servidor host.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b5a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b5a3-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b5a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b5a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5a3-106">O cmdlet **use-AzureRmSqlServerAuditingPolicy** especifica que um banco de dados usa a política de auditoria do servidor host.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="0b5a3-107">Especifique os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0b5a3-108">Se não houver nenhuma política de auditoria definida para o servidor de banco de dados, esse cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="0b5a3-109">Se o host usar a auditoria no nível do servidor, a detecção de ameaças será removida.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="0b5a3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b5a3-110">EXAMPLES</span></span>

### <span data-ttu-id="0b5a3-111">Exemplo 1: configurar um banco de dados para usar a política de auditoria do servidor</span><span class="sxs-lookup"><span data-stu-id="0b5a3-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="0b5a3-112">Esse comando especifica que o banco de dados chamado Database01 no Server02 usa a política de auditoria do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="0b5a3-113">OS</span><span class="sxs-lookup"><span data-stu-id="0b5a3-113">PARAMETERS</span></span>

### <span data-ttu-id="0b5a3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b5a3-114">-DatabaseName</span></span>
<span data-ttu-id="0b5a3-115">Especifica o nome do banco de dados que vai usar a política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-115">Specifies the name of the database that will use the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5a3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b5a3-116">-PassThru</span></span>
<span data-ttu-id="0b5a3-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b5a3-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b5a3-120">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0b5a3-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0b5a3-121">-ServerName</span></span>
<span data-ttu-id="0b5a3-122">Especifica o nome do servidor que hospeda o banco de dados que usa a política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="0b5a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5a3-123">-DefaultProfile</span></span>
<span data-ttu-id="0b5a3-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5a3-125">CommonParameters</span></span>
<span data-ttu-id="0b5a3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b5a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5a3-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5a3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5a3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b5a3-128">INPUTS</span></span>

## <span data-ttu-id="0b5a3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b5a3-129">OUTPUTS</span></span>

### <span data-ttu-id="0b5a3-130">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0b5a3-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="0b5a3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b5a3-131">NOTES</span></span>

## <span data-ttu-id="0b5a3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b5a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b5a3-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5a3-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="0b5a3-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5a3-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0b5a3-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5a3-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="0b5a3-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5a3-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0b5a3-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0b5a3-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


