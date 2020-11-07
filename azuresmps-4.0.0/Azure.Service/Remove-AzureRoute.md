---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946135"
---
# <span data-ttu-id="13a8c-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="13a8c-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="13a8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="13a8c-103">Remove uma rota de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="13a8c-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="13a8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13a8c-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="13a8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="13a8c-106">O cmdlet **Remove-AzureRoute** remove uma rota de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="13a8c-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="13a8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13a8c-107">EXAMPLES</span></span>

### <span data-ttu-id="13a8c-108">Exemplo 1: remover uma rota</span><span class="sxs-lookup"><span data-stu-id="13a8c-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="13a8c-109">Esse comando obtém uma tabela de rota chamada ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="13a8c-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="13a8c-110">O comando transmite essa tabela de rota para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="13a8c-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="13a8c-111">O cmdlet atual remove uma rota chamada InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="13a8c-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="13a8c-112">OS</span><span class="sxs-lookup"><span data-stu-id="13a8c-112">PARAMETERS</span></span>

### <span data-ttu-id="13a8c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="13a8c-113">-Force</span></span>
<span data-ttu-id="13a8c-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="13a8c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a8c-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="13a8c-115">-Profile</span></span>
<span data-ttu-id="13a8c-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="13a8c-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="13a8c-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="13a8c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13a8c-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="13a8c-118">-RouteName</span></span>
<span data-ttu-id="13a8c-119">Especifica um nome para a nova rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="13a8c-119">Specifies a name for the new route that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a8c-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="13a8c-120">-RouteTable</span></span>
<span data-ttu-id="13a8c-121">Especifica a tabela de rotas da qual esse cmdlet Remove uma rota.</span><span class="sxs-lookup"><span data-stu-id="13a8c-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13a8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a8c-122">CommonParameters</span></span>
<span data-ttu-id="13a8c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a8c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a8c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a8c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13a8c-125">INPUTS</span></span>

## <span data-ttu-id="13a8c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13a8c-126">OUTPUTS</span></span>

## <span data-ttu-id="13a8c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13a8c-127">NOTES</span></span>

## <span data-ttu-id="13a8c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13a8c-128">RELATED LINKS</span></span>

[<span data-ttu-id="13a8c-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="13a8c-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


