---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945571"
---
# <span data-ttu-id="1ba96-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1ba96-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="1ba96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ba96-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba96-103">Obtém informações sobre os servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba96-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="1ba96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba96-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ba96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ba96-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba96-106">O cmdlet **Get-AzureSqlDatabaseServer** Obtém informações sobre as instâncias do servidor de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1ba96-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="1ba96-107">Se você especificar um servidor por nome, esse cmdlet retornará um objeto que contém informações sobre esse servidor.</span><span class="sxs-lookup"><span data-stu-id="1ba96-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="1ba96-108">Caso contrário, o cmdlet retorna informações sobre todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="1ba96-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="1ba96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ba96-109">EXAMPLES</span></span>

### <span data-ttu-id="1ba96-110">Exemplo 1: obter informações sobre todos os servidores</span><span class="sxs-lookup"><span data-stu-id="1ba96-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="1ba96-111">Esse comando retorna informações sobre todas as instâncias do servidor de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1ba96-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="1ba96-112">Exemplo 2: obter informações sobre um servidor específico</span><span class="sxs-lookup"><span data-stu-id="1ba96-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="1ba96-113">Esse comando retorna informações sobre o servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="1ba96-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="1ba96-114">OS</span><span class="sxs-lookup"><span data-stu-id="1ba96-114">PARAMETERS</span></span>

### <span data-ttu-id="1ba96-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1ba96-115">-Profile</span></span>
<span data-ttu-id="1ba96-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1ba96-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ba96-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1ba96-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba96-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1ba96-118">-ServerName</span></span>
<span data-ttu-id="1ba96-119">Especifica o nome do servidor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1ba96-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="1ba96-120">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="1ba96-120">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba96-121">CommonParameters</span></span>
<span data-ttu-id="1ba96-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba96-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba96-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba96-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ba96-124">INPUTS</span></span>

### <span data-ttu-id="1ba96-125">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="1ba96-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="1ba96-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ba96-126">OUTPUTS</span></span>

### <span data-ttu-id="1ba96-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="1ba96-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="1ba96-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ba96-128">NOTES</span></span>

## <span data-ttu-id="1ba96-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ba96-129">RELATED LINKS</span></span>

[<span data-ttu-id="1ba96-130">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1ba96-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="1ba96-131">Servidores de lista</span><span class="sxs-lookup"><span data-stu-id="1ba96-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="1ba96-132">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1ba96-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1ba96-133">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1ba96-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1ba96-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1ba96-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1ba96-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1ba96-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


